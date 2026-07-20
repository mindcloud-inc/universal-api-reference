# List Payments with GoAffPro

Retrieves payment history entries from GoAffPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/payments`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [List Payments](https://api.goaffpro.com/docs/admin/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_id` | query | `string` | no | Only return payments for this affiliate ID. |
| `fields[]` | query | `array<string>` | yes | Fields to include in returned payments. |
