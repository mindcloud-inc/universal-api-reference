# Send Transactional Message with External Content with Dynosend

Creates a transactional message in Dynosend with external content.

## Endpoint

- **Method:** `POST`
- **Path:** `/transactional`
- **Base URL:** `https://api.dynosend.com/api/v2`
- **Official documentation:** [Send Transactional Message with External Content](https://developers.dynosend.com/#sendamessage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `htmlBody` | body | `string` | yes | The HTML content to send when the transactional template uses external content. |
| `recipient` | body | `string` | yes | The email address that should receive the transactional message. |
| `textBody` | body | `string` | yes | The plain-text content to send when the transactional template uses external content. |
| `transactional_uid` | body | `string` | yes | The UID of the Dynosend transactional message to send. |
