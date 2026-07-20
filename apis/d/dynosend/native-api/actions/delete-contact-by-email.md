# Delete Contact by Email with Dynosend

Deletes a Dynosend contact by email address.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contacts`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Delete Contact by Email](https://developers.dynosend.com/#deleteacontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_uid` | query | `string` | yes | The UID of the audience that contains the contact. |
| `email` | query | `string` | yes | The email address of the contact to delete. |
