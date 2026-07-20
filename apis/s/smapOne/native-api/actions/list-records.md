# List records with smapOne

Retrieves data records from smapOne.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/Smaps/{smapId}/Versions/{version}/Data`
- **Base URL:** `https://platform.smapone.com/Backend`
- **Official documentation:** [List records](https://platform.smapone.com/swagger/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `format` | query | `string` | no | Optional output format such as json or xml. |
| `smapId` | path | `string` | yes | The smap id. |
| `state` | query | `string` | no | Optional record state filter: new, exported, or incomplete. |
| `version` | path | `string` | yes | The smap version in major or major.minor format. |
