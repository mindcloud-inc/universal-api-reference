# Delete records with smapOne

Deletes data records from a smapOne version.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/Smaps/{smapId}/Versions/{version}/Data`
- **Base URL:** `https://platform.smapone.com/Backend`
- **Official documentation:** [Delete records](https://platform.smapone.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `smapId` | path | `string` | yes | The smap id. |
| `state` | query | `string` | no | Optional record state filter: new, exported, or incomplete. |
| `version` | path | `string` | yes | The smap version in major or major.minor format. |
