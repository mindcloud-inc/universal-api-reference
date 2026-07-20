# Export Raw Scan Data with Scanova

## Endpoint

- **Method:** `POST`
- **Path:** `/analytics/qr/raw/`
- **Base URL:** `https://management.scanova.io`
- **Official documentation:** [Export Raw Scan Data](https://docs.scanova.io/api-reference/endpoint/analytics/export-raw)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `date` | yes | Start date for scan data (inclusive). Format: YYYY-MM-DD |
| `to` | query | `date` | yes | End date for scan data (inclusive). Format: YYYY-MM-DD. Defaults to current date. |
| `file_format` | query | `string` | yes | Export file format for the raw data. CSV is ideal for lightweight processing. |
| `filter_by` | body | `list` | yes | Filter by QR code ID or tags Accepted values: `qrid`, `tags`. |
| `q[]` | body | `array<string>` | yes | Array of QR code IDs (if filter_by is 'qrid') or tags (if filter_by is 'tags') to include in the raw export |
