# Get Package Benefits Detail Report with Zenoti

## Endpoint

- **Method:** `POST`
- **Path:** `reports/packages/benefits/flat_file`
- **Base URL:** `https://api.zenoti.com/v1/`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `centers[]` | body | `array` | no | — |
| `centers[].center` | body | `list` | no | — |
| `date_type` | body | `list` | no | — |
| `start_date` | body | `date` | no | — |
| `end_date` | body | `date` | no | Don't set end date when the Date Type is "Balance As On Date" |
| `includeTotal` | body | `boolean` | no | Format: `toggle`. |
