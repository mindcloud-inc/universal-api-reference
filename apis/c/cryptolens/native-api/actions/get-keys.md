# Get Keys with Cryptolens

Retrieves license keys for a product from Cryptolens.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/product/GetKeys`
- **Base URL:** `https://api.cryptolens.io`
- **Official documentation:** [Get Keys](https://app.cryptolens.io/docs/api/v3/GetKeys)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ProductId` | query | `number` | yes | The product id. |
| `Page` | query | `number` | no | If there are more than 100 keys, only 99 will be returned on the first page. Increment this parameter by 1 to obtain the remaining licenses. |
| `OrderBy` | query | `string` | no | Specifies the way to order the result. |
| `SearchQuery` | query | `string` | no | Restricts the result to only the license keys that satisfy the criterion. |
| `GlobalId` | query | `number` | no | If you need to find a specific license key, set this parameter to its ID for a faster response. |
