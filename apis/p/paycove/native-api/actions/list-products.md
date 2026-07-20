# List Products with Paycove

Retrieves products from Paycove.

## Endpoint

- **Method:** `GET`
- **Path:** `products`
- **Base URL:** `https://paycove.io/api/v1`
- **Official documentation:** [List Products](https://docs.paycove.io/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search term to filter products by name, description, or CRM product ID. |
