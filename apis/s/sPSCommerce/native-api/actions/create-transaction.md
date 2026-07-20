# Create Transaction with SPS Commerce

This API accepts a payload that initiates a new transaction.

## Endpoint

- **Method:** `POST`
- **Path:** `transactions/v5/data/:filePath`
- **Base URL:** `https://api.spscommerce.com/`
- **Official documentation:** [Create Transaction](https://developercenter.spscommerce.com/#/docs/transaction-api/v5-posting)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/octet-stream` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filePath` | path | `string` | yes | Full absolute path to the file (case sensitive) |
| `payload` | body | `string` | no | — |
