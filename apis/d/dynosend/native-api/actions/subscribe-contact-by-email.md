# Subscribe Contact by Email with Dynosend

Subscribes a Dynosend contact by email address.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/subscribe`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Subscribe Contact by Email](https://developers.dynosend.com/#subscribeacontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_uid` | body | `string` | yes | The UID of the audience that contains the contact. |
| `email` | body | `string` | yes | The email address of the contact to subscribe. |
