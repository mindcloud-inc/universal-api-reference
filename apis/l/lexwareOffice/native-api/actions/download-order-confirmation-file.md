# Download Order Confirmation File with Lexware Office

Downloads an order confirmation file from Lexware Office.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/order-confirmations/:id/file`
- **Base URL:** `https://api.lexware.io`
- **Official documentation:** [Download Order Confirmation File](https://developers.lexware.io/docs/#order-confirmations-endpoint-download-an-order-confirmation-file)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `*/*` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Lexware order confirmation ID. |
