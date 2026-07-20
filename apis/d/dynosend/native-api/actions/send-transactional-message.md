# Send Transactional Message with Dynosend

Creates a transactional message in Dynosend.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactional`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Send Transactional Message](https://developers.dynosend.com/#sendamessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recipient` | body | `string` | yes | The email address that should receive the transactional message. |
| `transactional_uid` | body | `string` | yes | The UID of the Dynosend transactional message to send. |
