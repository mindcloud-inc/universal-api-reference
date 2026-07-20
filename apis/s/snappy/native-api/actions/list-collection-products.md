# List Collection Products with Snappy

Retrieves products from a specific Snappy collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/collections/{collectionId}/products`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [List Collection Products](https://docs.snappy.com/reference/getcollectionproducts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Collection ID. |
| `minBudget` | query | `number` | yes | Minimum budget. |
| `maxBudget` | query | `number` | yes | Maximum budget. |
| `companyId` | query | `string` | no | Company ID. |
| `country` | query | `string` | no | Country. |
| `accountId` | query | `string` | no | Account ID. |
| `fields[]` | query | `array<string>` | no | Additional product fields to include. |
| `skip` | query | `number` | no | Number of records to skip for pagination. |
| `limit` | query | `number` | no | Maximum number of records to return per page. |
