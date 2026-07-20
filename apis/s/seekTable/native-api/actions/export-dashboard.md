# Export Dashboard with SeekTable

Exports a SeekTable dashboard in the requested format.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/dashboard/:dashboard_id/export`
- **Base URL:** `https://www.seektable.com`
- **Official documentation:** [Export Dashboard](https://www.seektable.com/help/web-api-integration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dashboard_id` | path | `string` | yes | GUID of the dashboard in your SeekTable account. |
| `format` | query | `string` | yes | Export format for the generated dashboard file. Accepted values: `0`, `1`. |
| `report_parameters` | query | `string` | no | JSON object string with report parameter values. Requires Advanced Publishing. |
