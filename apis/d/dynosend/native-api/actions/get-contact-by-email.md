# Get Contact by Email with Dynosend

Retrieves a contact from Dynosend by email address.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Get Contact by Email](https://developers.dynosend.com/#getacontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_uid` | query | `string` | yes | The UID of the audience that contains the contact. |
| `email` | query | `string` | yes | The email address of the contact to fetch. |
