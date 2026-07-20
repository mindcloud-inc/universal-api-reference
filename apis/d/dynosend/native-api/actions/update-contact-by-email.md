# Update Contact by Email with Dynosend

Updates a contact in Dynosend by email address.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/update`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Update Contact by Email](https://developers.dynosend.com/#updateacontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_uid` | body | `string` | yes | The UID of the audience that contains the contact. |
| `email` | body | `string` | yes | The email address of the contact to update. |
| `new_email` | body | `string` | no | A replacement email address for the contact. |
| `tag` | body | `string` | no | A comma-separated tag list that replaces the contact's current tags. |
