# List Stock Adjustment Documents with Sumtracker

Retrieves stock adjustment documents from Sumtracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/version/2025-03/stock/adjustment/documents/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [List Stock Adjustment Documents](https://developers.sumtracker.com/reference/stockadjustmentdocumentlist)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `adjustment_type` | query | `string` | no |
| `created_range_after` | query | `date` | no |
| `created_range_before` | query | `date` | no |
| `is_complete` | query | `boolean` | no |
| `is_task_in_progress` | query | `boolean` | no |
| `limit` | query | `number` | no |
| `notes` | query | `string` | no |
| `number` | query | `string` | no |
| `o[]` | query | `array<string>` | no |
| `o[]ffset` | query | `number` | no |
| `o[]rdering` | query | `string` | no |
| `reason` | query | `string` | no |
| `updated_range_after` | query | `date` | no |
| `updated_range_before` | query | `date` | no |
| `warehouse` | query | `number` | no |
