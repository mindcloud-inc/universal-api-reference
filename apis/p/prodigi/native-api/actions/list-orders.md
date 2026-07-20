# List Orders with Prodigi

Retrieves a list of orders from Prodigi.

## Endpoint

- **Method:** `GET`
- **Path:** `/orders`
- **Base URL:** `https://api.prodigi.com/v4.0`
- **Official documentation:** [List Orders](https://www.prodigi.com/print-api/docs/reference/#get-orders)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdFrom` | query | `date` | no | Limit to orders placed after this UTC date/time. |
| `createdTo` | query | `date` | no | Limit to orders placed before this UTC date/time. |
| `status` | query | `string` | no | Limit to a status: draft, awaitingPayment, inProgress, complete, or cancelled. |
| `orderIds[]` | query | `array<string>` | no | Limit to a list of Prodigi order IDs. Send multiple values as a array. |
| `merchantReferences[]` | query | `array<string>` | no | Limit to a list of merchant order references. Send multiple values as a array. |
