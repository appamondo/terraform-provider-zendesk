---
# generated by https://github.com/hashicorp/terraform-plugin-docs
page_title: "zendesk_group Resource - terraform-provider-zendesk"
subcategory: ""
description: |-
  Provides a group resource.
---

# zendesk_group (Resource)

Provides a group resource.

## Example Usage

```terraform
# API reference:
#   https://developer.zendesk.com/rest_api/docs/support/groups

resource "zendesk_group" "moderator-group" {
  name = "Moderator"
}

resource "zendesk_group" "developer-group" {
  name = "Developer"
}
```

<!-- schema generated by tfplugindocs -->
## Schema

### Required

- `name` (String) Group name.

### Optional

- `id` (String) The ID of this resource.

### Read-Only

- `url` (String)

