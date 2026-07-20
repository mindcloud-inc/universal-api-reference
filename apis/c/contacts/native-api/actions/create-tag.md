# Create Tag with Contacts+

Creates a new tag in Contacts+.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/tags.create`
- **Base URL:** `https://api.contactsplus.com`
- **Official documentation:** [Create Tag](https://www.contactsplus.com/developers/contacts-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `tag` | body | `object` | yes | The tag object to create. |
| `teamId` | body | `string` | no | Create the tag in this team instead of personal tags. |
