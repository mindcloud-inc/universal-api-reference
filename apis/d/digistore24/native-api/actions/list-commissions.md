# List Commissions with Digistore24

Retrieves a list of commission amounts from Digistore24.

## Endpoint

- **Method:** `GET`
- **Path:** `/listCommissions`
- **Base URL:** `https://www.digistore24.com/api/call`
- **Official documentation:** [List Commissions](https://digistore24.com/api/docs/paths/listCommissions.yaml)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `string` | no | Start date/time |
| `to` | query | `string` | no | End date/time |
| `page_no` | query | `number` | no | Page number |
| `page_size` | query | `number` | no | Page size |
| `transaction_type` | query | `string` | no | Transaction type |
| `commission_type` | query | `string` | no | Commission type |
| `purchase_id` | query | `string` | no | Purchase ID |
