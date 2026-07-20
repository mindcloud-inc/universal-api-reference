# Get record with smapOne

Retrieves a data record from smapOne.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/Smaps/{smapId}/Versions/{version}/Data/{recordId}`
- **Base URL:** `https://platform.smapone.com/Backend`
- **Official documentation:** [Get record](https://platform.smapone.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | query | `string` | no | Optional output format such as json or xml. |
| `recordId` | path | `string` | yes | The data record id. |
| `smapId` | path | `string` | yes | The smap id. |
| `version` | path | `string` | yes | The smap version in major or major.minor format. |
