# Get Collection Product with Snappy

Retrieves a product from a specific Snappy collection.

## Endpoint

- **Method:** `GET`
- **Path:** `/collections/{collectionId}/products/{productId}`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [Get Collection Product](https://docs.snappy.com/reference/getcollectionproduct)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `collectionId` | path | `string` | yes | Collection ID. |
| `productId` | path | `string` | yes | Product ID. |
| `minBudget` | query | `number` | no | Minimum budget. |
| `maxBudget` | query | `number` | no | Maximum budget. |
| `companyId` | query | `string` | no | Company ID. |
| `country` | query | `string` | no | Country. |
| `accountId` | query | `string` | no | Account ID. |
| `fields[]` | query | `array<string>` | no | Additional product fields to include. |
