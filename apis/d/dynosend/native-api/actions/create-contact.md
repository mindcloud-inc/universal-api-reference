# Create Contact with Dynosend

Creates a new contact in Dynosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Create Contact](https://developers.dynosend.com/#createacontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_uid` | body | `string` | yes | The UID of the audience where the contact will be created. |
| `EMAIL` | body | `string` | yes | The email address of the contact to create. |
