# Get Asset Import Progress with Fleetworthy

## Endpoint

- **Method:** `GET`
- **Path:** `/assets/bulk/import/progress/:importProcessId`
- **Base URL:** `https://apis.fleetworthy.com/compliance-api/v1`
- **Official documentation:** [Get Asset Import Progress](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-assets-bulk-import-progress-importprocessid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `importProcessId` | path | `string` | yes | The unique identifier of the import process to check. |
