# Update Contact Photo with Google Contacts

Updates a contact photo in Google Contacts.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/people/:resourceName:photoAction`
- **Base URL:** `https://people.googleapis.com`
- **Official documentation:** [Update Contact Photo](https://developers.google.com/people/api/rest/v1/people/updateContactPhoto)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resourceName` | path | `string` | yes | — |
| `photoBytes` | body | `string` | yes | Base64-encoded photo bytes. |
