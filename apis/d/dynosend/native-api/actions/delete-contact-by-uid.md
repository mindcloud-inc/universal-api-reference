# Delete Contact by UID with Dynosend

Deletes a Dynosend contact by UID.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contacts`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Delete Contact by UID](https://developers.dynosend.com/#deleteacontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_uid` | query | `string` | yes | The UID of the audience that contains the contact. |
| `contact_uid` | query | `string` | yes | The UID of the contact to delete. |
