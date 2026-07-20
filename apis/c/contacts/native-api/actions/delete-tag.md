# Delete Tag with Contacts+

Deletes an existing tag from Contacts+.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tags.delete`
- **Base URL:** `https://api.contactsplus.com`
- **Official documentation:** [Delete Tag](https://www.contactsplus.com/developers/contacts-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tagId` | body | `string` | yes | The tag ID to delete. |
| `etag` | body | `string` | yes | The current tag ETag. |
| `teamId` | body | `string` | no | Delete the tag from this team instead of personal tags. |
