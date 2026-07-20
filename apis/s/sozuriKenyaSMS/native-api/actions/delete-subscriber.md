# Delete Subscriber with Sozuri (Kenya) SMS

Deactivates a premium SMS subscriber in Sozuri.

## Endpoint

- **Method:** `POST`
- **Path:** `/premium`
- **Base URL:** `https://sozuri.net/api/v1`
- **Official documentation:** [Delete Subscriber](https://sozuri.net/docs/subscription)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `shortcode` | body | `string` | yes | The premium shortcode for the service. |
| `keyword` | body | `string` | yes | The premium service keyword. |
| `number` | body | `string` | yes | The subscriber phone number in E.164 format. |
| `network` | body | `string` | yes | The subscriber mobile network, for example safaricom. |
