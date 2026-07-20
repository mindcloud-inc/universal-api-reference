# Lookup Order By External Order ID with WeSupply

Retrieves an order from WeSupply by external order ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/lookup`
- **Base URL:** `https://{subdomain}.labs.wesupply.xyz/api`
- **Official documentation:** [Lookup Order By External Order ID](https://documenter.getpostman.com/view/11859344/T17AiAYq#e5cc24f3-c4e7-4daf-9f76-94753c120062)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `OrderExternalOrderID` | query | `string` | no | The external order ID to look up in WeSupply. |
