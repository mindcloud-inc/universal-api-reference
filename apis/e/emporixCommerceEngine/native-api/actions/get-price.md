# Get Price with Emporix Commerce Engine

Retrieves a price from Emporix Commerce Engine.

## Endpoint

- **Method:** `GET`
- **Path:** `/price/{tenantId}/prices/:priceId`
- **Base URL:** `https://api.emporix.io`
- **Official documentation:** [Get Price](https://raw.githubusercontent.com/emporix/api-references/refs/heads/main/prices-and-taxes/price-service/api-reference/api.yml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `priceId` | path | `string` | yes | The unique ID of the price. |
