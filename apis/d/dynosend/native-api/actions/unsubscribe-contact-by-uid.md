# Unsubscribe Contact by UID with Dynosend

Unsubscribes a Dynosend contact by UID.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/unsubscribe`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Unsubscribe Contact by UID](https://developers.dynosend.com/#unsubscribeacontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_uid` | body | `string` | yes | The UID of the audience that contains the contact. |
| `contact_uid` | body | `string` | yes | The UID of the contact to unsubscribe. |
