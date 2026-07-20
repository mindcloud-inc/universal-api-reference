# Subscribe Contact by UID with Dynosend

Subscribes a Dynosend contact by UID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/subscribe`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Subscribe Contact by UID](https://developers.dynosend.com/#subscribeacontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_uid` | body | `string` | yes | The UID of the audience that contains the contact. |
| `contact_uid` | body | `string` | yes | The UID of the contact to subscribe. |
