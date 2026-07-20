# Export Calls CSV with CallScaler

Downloads a calls CSV export from CallScaler.

## Endpoint

- **Method:** `GET`
- **Path:** `/calls/export`
- **Base URL:** `https://callscaler.com/api/v1`
- **Official documentation:** [Export Calls CSV](https://callscaler.com/docs/api-calls)

## Capabilities

This operation supports [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `end_date` | query | `date` | no |
| `qualified` | query | `boolean` | no |
| `source` | query | `string` | no |
| `start_date` | query | `date` | no |
| `status` | query | `string` | no |
