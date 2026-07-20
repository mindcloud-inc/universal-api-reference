# Export Report with SeekTable

Exports a SeekTable report in the requested format.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/report/:report_id/export`
- **Base URL:** `https://www.seektable.com`
- **Official documentation:** [Export Report](https://www.seektable.com/help/web-api-integration)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `report_id` | path | `string` | yes | GUID of the report in your SeekTable account. |
| `format` | query | `string` | yes | Export format for the generated report file. Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`. |
| `report_parameters` | query | `string` | no | JSON object string with report parameter values. Requires Advanced Publishing. |
| `html_inline_style` | query | `boolean` | no | Enable inline styles in HTML output. |
| `chart_only` | query | `boolean` | no | Render only chart output for pdf or png exports. |
| `value_formatting` | query | `boolean` | no | Whether exported values should use SeekTable value formatting. |
| `row_mode` | query | `string` | no | JSON export only: determines whether rows are serialized as arrays or objects. Accepted values: `0`, `1`. |
