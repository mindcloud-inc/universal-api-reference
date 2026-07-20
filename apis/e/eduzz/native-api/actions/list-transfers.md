# List Transfers with Eduzz

Retrieves transfer details from Eduzz using the provided filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/myeduzz/v1/financial/transfers`
- **Base URL:** `https://api.eduzz.com`
- **Official documentation:** [List Transfers](https://developers.eduzz.com/reference/api/get-myeduzz-v1-financial-transfers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `endDate` | query | `string` | yes | Include transfers through this date. |
| `startDate` | query | `string` | yes | Include transfers from this date onward. |
