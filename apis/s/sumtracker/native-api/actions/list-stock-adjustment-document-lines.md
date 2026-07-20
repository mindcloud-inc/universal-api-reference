# List Stock Adjustment Document Lines with Sumtracker

Retrieves stock adjustment document lines from Sumtracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/version/2025-03/stock/adjustment/documents/:document_id/lines/`
- **Base URL:** `https://inventory-api.sumtracker.com`
- **API:** REST - Page Based
- **Official documentation:** [List Stock Adjustment Document Lines](https://developers.sumtracker.com/reference/stockadjustmentdocumentlinelist)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `document_id` | path | `string` | yes | Stock adjustment document ID. |
