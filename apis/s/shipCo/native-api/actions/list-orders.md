# List Orders with Ship&Co

## Endpoint

- **Method:** `GET`
- **Path:** `/orders`
- **Base URL:** `https://api.shipandco.com/v1`
- **Official documentation:** [List Orders](https://developer.shipandco.com/en/#order)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `created_after` | query | `date` | no | Only include orders created after this ISO timestamp. |
| `created_before` | query | `date` | no | Only include orders created before this ISO timestamp. |
