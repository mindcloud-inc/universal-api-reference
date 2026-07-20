# Download Verification Report with MillionVerifier

Downloads a verification report from MillionVerifier.

## Endpoint

- **Method:** `GET`
- **Path:** `https://bulkapi.millionverifier.com/bulkapi/v2/download`
- **Base URL:** `https://api.millionverifier.com`
- **Official documentation:** [Download Verification Report](https://developer.millionverifier.com/#operation/bulk-download)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file_id` | query | `number` | yes | The ID of the uploaded file. |
| `filter` | query | `string` | yes | Report filter preset. |
| `statuses` | query | `string` | no | Comma-separated statuses to include when filter is custom. |
| `free` | query | `string` | no | Whether to include only free or non-free domains when filter is custom. |
| `role` | query | `string` | no | Whether to include only role or non-role emails when filter is custom. |
