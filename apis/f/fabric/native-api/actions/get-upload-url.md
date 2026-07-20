# Get Upload URL with Fabric

Retrieves an upload URL from Fabric.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/upload`
- **Base URL:** `https://api.fabric.so`
- **Official documentation:** [Get Upload URL](https://developers.fabric.so/api-reference/tag/uploads/get/v2/upload)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filename` | query | `string` | yes | Name of the file to upload to Fabric. |
| `size` | query | `number` | yes | Size of the file in bytes. |
