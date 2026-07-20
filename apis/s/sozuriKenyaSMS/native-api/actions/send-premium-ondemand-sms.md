# Send Premium Ondemand SMS with Sozuri (Kenya) SMS

Sends an on-demand premium SMS through Sozuri.

## Endpoint

- **Method:** `POST`
- **Path:** `/premium`
- **Base URL:** `https://sozuri.net/api/v1`
- **Official documentation:** [Send Premium Ondemand SMS](https://sozuri.net/docs/ondemand)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | body | `string` | yes | The premium shortcode sender defined in your project. |
| `to` | body | `string` | yes | A recipient phone number in E.164 format. |
| `campaign` | body | `string` | no | The campaign name for this message. |
| `message` | body | `string` | yes | The premium SMS content to send. |
| `linkId` | body | `string` | yes | The link ID received from the inbound ondemand notification. |
| `keyword` | body | `string` | yes | The premium service keyword. |
