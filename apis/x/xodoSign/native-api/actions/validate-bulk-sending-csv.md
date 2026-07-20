# Validate Bulk Sending CSV with Xodo Sign

Validates a bulk sending CSV for a template in Xodo Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/template/:templateHash/bulk/csv/validate`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Validate Bulk Sending CSV](https://eversign.com/api/documentation/methods#validate-bulk-sending-csv)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the template. |
| `templateHash` | path | `string` | yes | The template hash to validate the CSV against. |
| `csv_with_bulk_data` | body | `file` | yes | The CSV file to validate as multipart form-data. |
