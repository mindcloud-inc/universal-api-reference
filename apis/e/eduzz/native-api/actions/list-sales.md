# List Sales with Eduzz

Retrieves sales from Eduzz using the provided filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/myeduzz/v1/sales`
- **Base URL:** `https://api.eduzz.com`
- **Official documentation:** [List Sales](https://developers.eduzz.com/reference/api/get-myeduzz-v1-sales)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliateId` | query | `string` | no | Filter sales by affiliate id. |
| `buyerDocument` | query | `string` | no | Filter sales by buyer document. |
| `buyerEmail` | query | `string` | no | Filter sales by buyer email. |
| `contractId` | query | `string` | no | Filter sales by contract id. |
| `endDate` | query | `string` | yes | Include sales through this date. |
| `productId` | query | `string` | no | Filter sales by product id. |
| `referenceDate` | query | `string` | no | Sales date basis accepted by Eduzz. |
| `startDate` | query | `string` | yes | Include sales from this date onward. |
| `status` | query | `string` | no | Filter sales by status. |
