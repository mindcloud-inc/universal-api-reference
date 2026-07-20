# List Products with QADeputy

Retrieves products from QADeputy.

## Endpoint

- **Method:** `GET`
- **Path:** `/products`
- **Base URL:** `https://app.qadeputy.com/api/v1`
- **Official documentation:** [List Products](https://apidocs.qadeputy.com/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `product_status` | query | `list` | no | Optional status filter. QADeputy documents active and archived products; the API defaults to active. Accepted values: `0`, `1`. |
