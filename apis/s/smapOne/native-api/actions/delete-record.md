# Delete record with smapOne

Deletes an existing data record from smapOne.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/Smaps/{smapId}/Versions/{version}/Data/{recordId}`
- **Base URL:** `https://platform.smapone.com/Backend`
- **Official documentation:** [Delete record](https://platform.smapone.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recordId` | path | `string` | yes | The data record id. |
| `smapId` | path | `string` | yes | The smap id. |
| `version` | path | `string` | yes | The smap version in major or major.minor format. |
