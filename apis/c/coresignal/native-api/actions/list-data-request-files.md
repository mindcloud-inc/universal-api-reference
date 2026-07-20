# List Data Request Files with Coresignal

Retrieves files for a bulk data request from Coresignal.

## Endpoint

- **Method:** `GET`
- **Path:** `/data_requests/:dataRequestId/files`
- **Base URL:** `https://api.coresignal.com/cdapi/v2`
- **Official documentation:** [List Data Request Files](https://docs.coresignal.com/api-introduction/download-center-and-bulk-data-requests)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dataRequestId` | path | `string` | yes | Data request identifier returned by a bulk collect action. |
