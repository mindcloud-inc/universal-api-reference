# Remove Tags From Contacts with Keap

## Endpoint

- **Method:** `POST`
- **Path:** `/tags/{tag_id}/contacts:removeTags`
- **Base URL:** `https://api.infusionsoft.com/crm/rest/v2`
- **Official documentation:** [Remove Tags From Contacts](https://developer.keap.com/docs/restv2/#tag/Tag/operation/removeTags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_ids` | body | `list<string>` | yes | Array of contact IDs to remove the tag from. |
| `tag_id` | path | `string` | yes | The unique identifier of the tag. |
