# Get File URL with SmartSuite

Retrieves a shared file URL from SmartSuite.

## Endpoint

- **Method:** `GET`
- **Path:** `/shared-files/:fileHandle/url/`
- **Base URL:** `https://app.smartsuite.com/api/v1`
- **Official documentation:** [Get File URL](https://developers.smartsuite.com/docs/solution-data/records/get-file-url)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileHandle` | path | `string` | yes | The SmartSuite file handle to exchange for a temporary download URL. |
