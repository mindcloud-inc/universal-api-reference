# List Quotes with Invoice Ninja

## Endpoint

- **Method:** `GET`
- **Path:** `/quotes`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [List Quotes](https://api-docs.invoicing.co/#tag/quotes/operation/getQuotes)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional status filter such as active, archived, or deleted. |
| `client_id` | query | `string` | no | Optional client filter using the hashed client ID. |
