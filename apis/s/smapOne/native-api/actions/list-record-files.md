# List record files with smapOne

Retrieves record file metadata from smapOne.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/Smaps/{smapId}/Versions/{version}/Data/{recordId}/Files`
- **Base URL:** `https://platform.smapone.com/Backend`
- **Official documentation:** [List record files](https://platform.smapone.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recordId` | path | `string` | yes | The data record id. |
| `smapId` | path | `string` | yes | The smap id. |
| `version` | path | `string` | yes | The smap version in major or major.minor format. |
