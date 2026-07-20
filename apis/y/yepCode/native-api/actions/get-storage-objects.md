# Get storage objects with YepCode

Retrieves storage object records from YepCode.

## Endpoint

- **Method:** `GET`
- **Path:** `/storage/objects`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Get storage objects](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Storage/getStorageObjects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `prefix` | query | `string` | no | Filter results to include only objects whose names begin with this prefix. |
