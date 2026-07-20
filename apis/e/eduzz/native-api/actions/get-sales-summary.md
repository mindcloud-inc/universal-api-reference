# Get Sales Summary with Eduzz

Retrieves a sales summary from Eduzz using provided filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/myeduzz/v1/sales/summary`
- **Base URL:** `https://api.eduzz.com`
- **Official documentation:** [Get Sales Summary](https://developers.eduzz.com/reference/api/get-myeduzz-v1-sales-summary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliateId` | query | `string` | no | Filter summary by affiliate id. |
| `contractId` | query | `string` | no | Filter summary by contract id. |
| `endDate` | query | `string` | yes | Include sales through this date. |
| `productId` | query | `string` | no | Filter summary by product id. |
| `startDate` | query | `string` | yes | Include sales from this date onward. |
| `status` | query | `string` | no | Filter summary by sale status. |
