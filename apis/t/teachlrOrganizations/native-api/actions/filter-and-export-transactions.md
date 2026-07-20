# Filter And Export Transactions with Teachlr Organizations

## Endpoint

- **Method:** `GET`
- **Path:** `/transactions`
- **Base URL:** `https://api.teachlr.com/mindcloudteachlr337933/api`
- **Official documentation:** [Filter And Export Transactions](https://soporte.teachlr.com/base-de-conocimientos/como-listar-las-transacciones-de-una-escuela-usando-el-api-de-teachlr-organizaciones-2/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `currency` | query | `string` | no | Filter transactions by currency. |
| `date_from` | query | `string` | no | Filter transactions created on or after this date. |
| `date_to` | query | `string` | no | Filter transactions created on or before this date. |
| `format` | query | `string` | no | Optional export format. |
| `item_type` | query | `string` | no | Filter transactions by item type. |
| `search` | query | `string` | no | Search text for transactions. |
| `sort` | query | `string` | no | Transaction field to sort by. |
| `status` | query | `string` | no | Filter transactions by status. |
| `ord` | query | `string` | no | Sort direction. |
