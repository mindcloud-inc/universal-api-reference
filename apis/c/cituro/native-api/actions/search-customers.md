# Search Customers with Cituro

Finds matching customer records in Cituro.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://app.cituro.com/api`
- **Official documentation:** [Search Customers](https://www.cituro.com/help/developers-corner/schnittstellen)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Filter customers by email address. |
| `lastName` | query | `string` | no | Filter customers by last name. |
| `limit` | query | `string` | no | Maximum number of customers to return. |
| `search` | query | `string` | no | Free-text customer search term. |
