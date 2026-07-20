# Get QR Code Analytics with Scanova

## Endpoint

- **Method:** `POST`
- **Path:** `/analytics/qr/`
- **Base URL:** `https://management.scanova.io`
- **Official documentation:** [Get QR Code Analytics](https://docs.scanova.io/api-reference/endpoint/analytics/qr-code)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | query | `string` | no | Analytics type(s) to retrieve. Multiple values can be comma-separated. Send multiple values as a string separated by `,`. |
| `from` | query | `date` | yes | Start date for analytics data (inclusive). Format: YYYY-MM-DD |
| `to` | query | `date` | yes | End date for analytics data (inclusive). Format: YYYY-MM-DD. Defaults to current date. |
| `filter_by` | body | `list` | yes | Filter by QR code ID or tags Accepted values: `qrid`, `tags`. |
| `q[]` | body | `array<string>` | yes | Array of QR code IDs (if filter_by is 'qrid') or tags (if filter_by is 'tags') |
