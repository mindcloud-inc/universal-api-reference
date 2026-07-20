# Lookup Orders By Customer Email with WeSupply

Finds orders in WeSupply by customer email.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders/lookup`
- **Base URL:** `https://{subdomain}.labs.wesupply.xyz/api`
- **Official documentation:** [Lookup Orders By Customer Email](https://documenter.getpostman.com/view/11859344/T17AiAYq#e5cc24f3-c4e7-4daf-9f76-94753c120062)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `CustomerEmail` | query | `string` | no | The customer email address to use for the order lookup. |
