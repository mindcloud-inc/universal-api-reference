# Get Contact Tag with Constant Contact

Retrieves a contact tag from Constant Contact.

## Endpoint

- **Method:** `GET`
- **Path:** `/contact_tags/:tag_id`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Get Contact Tag](https://developer.constantcontact.com/api_guide/tags_get_single.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag_id` | path | `string` | yes | UUID of the tag to retrieve. |
| `include_count` | query | `boolean` | no | Include contacts_count in the response. |
