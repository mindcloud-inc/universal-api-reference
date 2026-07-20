# Create Document Export with Billingo

Creates a new document export in Billingo.

## Endpoint

- **Method:** `POST`
- **Path:** `/document-export`
- **Base URL:** `https://api.billingo.hu/v3`
- **Official documentation:** [Create Document Export](https://api.swaggerhub.com/apis/Billingo/Billingo/3.0.15)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query_type` | body | `string` | yes | Date field used for the export range. Accepted values: `0`, `1`, `2`, `3`. |
| `start_date` | body | `date` | yes | Start date for the export range. |
| `end_date` | body | `date` | yes | End date for the export range. |
| `export_type` | body | `string` | yes | Billingo export format/type. |
