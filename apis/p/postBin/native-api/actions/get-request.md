# Get Request with PostBin

Retrieves a stored request from a PostBin bin.

## Endpoint

- **Method:** `GET`
- **Path:** `/bin/:binId/req/:reqId`
- **Base URL:** `https://www.postb.in/api/`
- **Official documentation:** [Get Request](https://www.postb.in/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `binId` | path | `string` | yes | The PostBin bin identifier. |
| `reqId` | path | `string` | yes | The request identifier returned by the capture endpoint. |
