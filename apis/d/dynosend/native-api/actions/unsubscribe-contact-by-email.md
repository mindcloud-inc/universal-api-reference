# Unsubscribe Contact by Email with Dynosend

Unsubscribes a Dynosend contact by email address.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/unsubscribe`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Unsubscribe Contact by Email](https://developers.dynosend.com/#unsubscribeacontact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience_uid` | body | `string` | yes | The UID of the audience that contains the contact. |
| `email` | body | `string` | yes | The email address of the contact to unsubscribe. |
