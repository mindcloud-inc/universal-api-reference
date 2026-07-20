# List Customers with Seven Time

Retrieves customers from a Seven Time workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://app.seventime.se/api/2`
- **Official documentation:** [List Customers](https://docs.seventime.se/#get-customers)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | no | — |
| `customerNumber` | query | `string` | no | — |
| `organizationNumber` | query | `string` | no | — |
| `city` | query | `string` | no | — |
| `lastModified` | query | `date` | no | Return customers modified since the provided timestamp. |
