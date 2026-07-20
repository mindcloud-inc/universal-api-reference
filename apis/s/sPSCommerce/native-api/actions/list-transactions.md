# List Transactions with SPS Commerce

Get a list of files in a specified directory.

## Endpoint

- **Method:** `GET`
- **Path:** `transactions/v5/data/:directoryPath`
- **Base URL:** `https://api.spscommerce.com/`
- **Official documentation:** [List Transactions](https://developercenter.spscommerce.com/#/docs/transaction-api/v5-filtering)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `directoryPath` | path | `string` | no | Full absolute path to the directory (case sensitive). - Must end with `/` character - Can be empty in case of `root` path |
| `entryNamePrefix` | query | `string` | no | Limit the response to entries that begin with the specified prefix (case sensitive) |
