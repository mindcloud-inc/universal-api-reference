# Update Tag with Contacts+

Updates an existing tag in Contacts+.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tags.update`
- **Base URL:** `https://api.contactsplus.com`
- **Official documentation:** [Update Tag](https://www.contactsplus.com/developers/contacts-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | body | `object` | yes | The tag object to update, including tagId and etag. |
| `teamId` | body | `string` | no | Update the tag in this team instead of personal tags. |
