# Get Asset By Guid with Active Network

Retrieves an asset by GUID in Active Network.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/search`
- **Base URL:** `http://api.amp.active.com`
- **Official documentation:** [Get Asset By Guid](https://developer.active.com/docs/read/v2_Activity_API_Search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `asset.assetGuid` | query | `string` | yes | Exact ACTIVE asset GUID to retrieve. |
