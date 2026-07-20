# Cancel Transfer with Dwolla

Cancels a pending transfer in Dwolla.

## Endpoint

- **Method:** `POST`
- **Path:** `/transfers/[:id]`
- **Base URL:** `https://api-sandbox.dwolla.com`
- **Official documentation:** [Cancel Transfer](https://developers.dwolla.com/docs/api-reference/transfers/cancel-a-transfer)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Dwolla transfer ID. |
