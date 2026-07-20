# Upload Contact Photo with Contacts+

Uploads a photo for an existing Contacts+ contact.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/contacts.uploadPhoto`
- **Base URL:** `https://api.contactsplus.com`
- **Official documentation:** [Upload Contact Photo](https://www.contactsplus.com/developers/contacts-api/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | body | `object` | yes | The contact object identifying which contact photo to upload. |
| `photoFile` | body | `file` | yes | The image file to upload as the contact photo. |
| `teamId` | body | `string` | no | Upload the photo to a team contact instead of personal contacts. |
