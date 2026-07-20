# List Products with Snappy

Retrieves products from Snappy.

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://api.snappy.com/public-api/v2`
- **Official documentation:** [List Products](https://docs.snappy.com/reference/getproducts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `minBudget` | query | `number` | yes | Minimum budget. |
| `maxBudget` | query | `number` | yes | Maximum budget. |
| `collectionId` | query | `string` | no | Collection ID. |
| `brandName` | query | `string` | no | Brand name. |
| `brands[]` | query | `array<string>` | no | List of product brand IDs. |
| `tags[]` | query | `array<string>` | no | List of hash tag IDs. |
| `title` | query | `string` | no | Product title. |
| `description` | query | `string` | no | Product description. |
| `skip` | query | `number` | no | Number of records to skip for pagination. |
| `limit` | query | `number` | no | Maximum number of records to return per page. |
| `companyId` | query | `string` | no | Company ID. |
| `country` | query | `string` | no | Country. |
| `accountId` | query | `string` | no | Account ID. |
| `fields[]` | query | `array<string>` | no | Additional product fields to include. |
