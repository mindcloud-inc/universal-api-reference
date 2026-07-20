# Shift Request with PostBin

Retrieves and removes the oldest request from a PostBin bin.

## Endpoint

- **Method:** `GET`
- **Path:** `/bin/:binId/req/shift`
- **Base URL:** `https://www.postb.in/api/`
- **Official documentation:** [Shift Request](https://www.postb.in/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `binId` | path | `string` | yes | The PostBin bin identifier. |
