# List Interests with Flexmail

Retrieves available contact interests from Flexmail.

## Endpoint

- **Method:** `GET`
- **Path:** `/interests`
- **Base URL:** `https://api.flexmail.eu`
- **Official documentation:** [List Interests](https://api.flexmail.eu/documentation/#get-/interests)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | query | `string` | no |
| `visibility` | query | `string` | no |
| `order_by` | query | `string` | no |
| `order_direction` | query | `string` | no |
