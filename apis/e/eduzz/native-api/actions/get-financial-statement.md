# Get Financial Statement with Eduzz

Retrieves a financial statement from Eduzz using provided filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/myeduzz/v2/financial/statement`
- **Base URL:** `https://api.eduzz.com`
- **Official documentation:** [Get Financial Statement](https://developers.eduzz.com/reference/api/get-myeduzz-v2-financial-statement)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | yes | Include statement entries through this date. |
| `saleId` | query | `string` | no | Filter statement entries by sale id. |
| `startDate` | query | `string` | yes | Include statement entries from this date onward. |
