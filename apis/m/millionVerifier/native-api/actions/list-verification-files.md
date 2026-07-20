# List Verification Files with MillionVerifier

Retrieves verification files from MillionVerifier.

## Endpoint

- **Method:** `GET`
- **Path:** `https://bulkapi.millionverifier.com/bulkapi/v2/filelist`
- **Base URL:** `https://api.millionverifier.com`
- **Official documentation:** [List Verification Files](https://developer.millionverifier.com/#operation/bulk-filelist)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `offset` | query | `number` | no | Offset for pagination. |
| `limit` | query | `number` | no | Maximum number of files to return. |
| `id` | query | `string` | no | Comma-separated file IDs to include. |
| `name` | query | `string` | no | Text that should appear in the file name. |
| `status` | query | `string` | no | Comma-separated file statuses to include. |
| `updated_at_from` | query | `string` | no | Only include files updated after this timestamp. |
| `updated_at_to` | query | `string` | no | Only include files updated before this timestamp. |
| `createdate_from` | query | `string` | no | Only include files created after this timestamp. |
| `createdate_to` | query | `string` | no | Only include files created before this timestamp. |
| `percent_from` | query | `number` | no | Only include files with progress greater than or equal to this percentage. |
| `percent_to` | query | `number` | no | Only include files with progress less than or equal to this percentage. |
| `has_error` | query | `string` | no | Filter for files that have or do not have errors. |
