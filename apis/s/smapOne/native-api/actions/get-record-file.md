# Get record file with smapOne

Retrieves a record file from smapOne.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/Smaps/{smapId}/Versions/{version}/Data/{recordId}/Files/{fileId}`
- **Base URL:** `https://platform.smapone.com/Backend`
- **Official documentation:** [Get record file](https://platform.smapone.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileId` | path | `string` | yes | The file id. |
| `recordId` | path | `string` | yes | The data record id. |
| `smapId` | path | `string` | yes | The smap id. |
| `version` | path | `string` | yes | The smap version in major or major.minor format. |
