# Get Realtime Status with Trint

Retrieves realtime transcript status from Trint.

## Endpoint

- **Method:** `GET`
- **Path:** `/transcripts/realtime/:trintId`
- **Base URL:** `https://api.trint.com`
- **Official documentation:** [Get Realtime Status](https://dev.trint.com/reference/get-realtime-status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `trintId` | path | `string` | yes | The Trint file identifier for the realtime transcript. |
