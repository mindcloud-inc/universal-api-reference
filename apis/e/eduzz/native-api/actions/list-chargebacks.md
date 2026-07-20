# List Chargebacks with Eduzz

Retrieves chargebacks from Eduzz using the provided filters.

## Endpoint

- **Method:** `GET`
- **Path:** `/myeduzz/v1/sales/chargebacks`
- **Base URL:** `https://api.eduzz.com`
- **Official documentation:** [List Chargebacks](https://developers.eduzz.com/reference/api/get-myeduzz-v1-sales-chargebacks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `buyerEmail` | query | `string` | no | Filter chargebacks by buyer email. |
| `chargebackStatus` | query | `string` | no | Filter chargebacks by status. |
| `endDate` | query | `string` | yes | Include chargebacks through this date. |
| `id` | query | `string` | no | Chargeback id. |
| `startDate` | query | `string` | yes | Include chargebacks from this date onward. |
