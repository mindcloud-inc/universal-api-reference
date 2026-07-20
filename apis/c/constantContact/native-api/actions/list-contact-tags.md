# List Contact Tags with Constant Contact

Retrieves contact tags from Constant Contact.

## Endpoint

- **Method:** `GET`
- **Path:** `/contact_tags`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [List Contact Tags](https://developer.constantcontact.com/api_guide/tags_get.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Number of tag results per page (up to 500). |
| `include_count` | query | `boolean` | no | Include contacts_count values in each tag result. |
