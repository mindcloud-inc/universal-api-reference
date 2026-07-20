# Update Contact Tag with Constant Contact

Renames a contact tag in Constant Contact.

## Endpoint

- **Method:** `PUT`
- **Path:** `/contact_tags/:tag_id`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Update Contact Tag](https://developer.constantcontact.com/api_guide/tags_update.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag_id` | path | `string` | yes | UUID of the tag to update. |
| `name` | body | `string` | yes | Updated tag name. |
