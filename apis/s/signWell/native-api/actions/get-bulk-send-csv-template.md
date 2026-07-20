# Get Bulk Send CSV Template with SignWell

Retrieves a bulk send CSV template from SignWell.

## Endpoint

- **Method:** `GET`
- **Path:** `/bulk_sends/csv_template`
- **Base URL:** `https://www.signwell.com/api/v1`
- **Official documentation:** [Get Bulk Send CSV Template](https://developers.signwell.com/reference/get_api-v1-bulk-sends-csv-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `template_ids[]` | query | `array<string>` | yes | One or more template IDs to generate a blank CSV template. |
| `base64` | query | `boolean` | no | When true, returns the CSV as a base64-encoded string in a JSON response. |
