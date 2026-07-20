# Delete Contact Tag with Constant Contact

Deletes a contact tag from Constant Contact.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contact_tags/:tag_id`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Delete Contact Tag](https://developer.constantcontact.com/api_guide/tags_delete.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag_id` | path | `string` | yes | UUID of the tag to delete. |
