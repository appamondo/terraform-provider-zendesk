---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "zendesk_attachment Resource - terraform-provider-zendesk"
subcategory: ""
description: |-
  Provides an attachment resource.
---

# zendesk_attachment (Resource)

Provides an attachment resource.

## Example Usage

```terraform
# API reference:
#   https://developer.zendesk.com/rest_api/docs/support/attachments

variable "logo_file_path" {
  type    = string
  default = "../zendesk/testdata/street.jpg"
}

resource "zendesk_attachment" "logo" {
  file_name = "street.jpg"
  file_path = var.logo_file_path
  file_hash = filesha256(var.logo_file_path)
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `file_hash` (String) SHA256 hash of the image file. Terraform built-in `filesha256()` is convenient to calculate it.
- `file_name` (String) The name of the image file.
- `file_path` (String)

### Optional

- `id` (String) The ID of this resource.

### Read-Only

- `content_type` (String) The content type of the image. Example value: "image/png"
- `content_url` (String) A full URL where the attachment image file can be downloaded. The file may be hosted externally so take care not to inadvertently send Zendesk authentication credentials.
- `inline` (Boolean) If true, the attachment is excluded from the attachment list and the attachment's URL can be referenced within the comment of a ticket. Default is false.
- `size` (Number) The size of the image file in bytes.
- `thumbnails` (Set of Object) A list of attachments. (see [below for nested schema](#nestedatt--thumbnails))
- `token` (String) The token of the uploaded attachment.

<a id="nestedatt--thumbnails"></a>
### Nested Schema for `thumbnails`

Read-Only:

- `content_type` (String)
- `content_url` (String)
- `file_name` (String)
- `id` (Number)
- `size` (Number)

