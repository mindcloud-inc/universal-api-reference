# Send Bulk SMS with Sozuri (Kenya) SMS

Sends bulk SMS messages through Sozuri.

## Endpoint

- **Method:** `POST`
- **Path:** `/messaging`
- **Base URL:** `https://sozuri.net/api/v1`
- **Official documentation:** [Send Bulk SMS](https://sozuri.net/docs/text)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | The sender ID defined in your project. |
| `to` | body | `string` | yes | A comma-separated list of recipient phone numbers in E.164 format. |
| `campaign` | body | `string` | no | The campaign name for this message. |
| `message` | body | `string` | yes | The SMS content to send. |
| `type` | body | `string` | yes | The sender ID type to use: promotional or transactional. |
