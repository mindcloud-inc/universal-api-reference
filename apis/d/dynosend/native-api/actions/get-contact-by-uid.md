# Get Contact by UID with Dynosend

Retrieves a contact from Dynosend by UID.

## Endpoint

- **Method:** `GET`
- **Path:** `/contacts`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Get Contact by UID](https://developers.dynosend.com/#getacontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_uid` | query | `string` | yes | The UID of the audience that contains the contact. |
| `contact_uid` | query | `string` | yes | The UID of the contact to fetch. |
