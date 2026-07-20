# Apply Tag To Contacts with Keap

## Endpoint

- **Method:** `POST`
- **Path:** `/tags/{tag_id}/contacts:applyTags`
- **Base URL:** `https://api.infusionsoft.com/crm/rest/v2`
- **Official documentation:** [Apply Tag To Contacts](https://developer.keap.com/docs/restv2/#tag/Tag/operation/applyTags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_ids` | body | `list<string>` | yes | Array of contact IDs to apply the tag to. |
| `tag_id` | path | `string` | yes | The unique identifier of the tag. |
