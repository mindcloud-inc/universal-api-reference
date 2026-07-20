# List Transactions with GoAffPro

Retrieves transaction log entries from GoAffPro.

## Endpoint

- **Method:** `GET`
- **Path:** `/admin/transactions`
- **Base URL:** `https://api.goaffpro.com/v1`
- **Official documentation:** [List Transactions](https://api.goaffpro.com/docs/admin/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `affiliate_id` | query | `string` | no | Only return transactions for this affiliate ID. |
| `type` | query | `string` | no | Only return transactions for this entity type. |
| `is_paid` | query | `boolean` | no | Only return transactions by payment status. |
