# List Customers with GorillaDesk

Retrieves customers from GorillaDesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers`
- **Base URL:** `https://api.gorilladesk.com/v1`
- **Official documentation:** [List Customers](https://api.gorilladesk.com)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_number` | query | `string` | no | Return results where the account_number field is equal this value. |
| `created[gt]` | query | `date` | no | — |
| `created[gte]` | query | `date` | no | — |
| `created[lt]` | query | `date` | no | — |
| `created[lte]` | query | `date` | no | — |
| `include[]` | query | `array<string>` | no | Send multiple values as a string separated by `,`. |
| `state[]` | query | `array<string>` | no | Send multiple values as a string separated by `,`. |
| `status[]` | query | `array<string>` | no | Send multiple values as a string separated by `,`. |
| `updated[gt]` | query | `date` | no | — |
| `updated[gte]` | query | `date` | no | — |
| `updated[lt]` | query | `date` | no | — |
| `updated[lte]` | query | `date` | no | — |
