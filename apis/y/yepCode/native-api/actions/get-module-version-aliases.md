# Get module version aliases with YepCode

Retrieves module version aliases from YepCode.

## Endpoint

- **Method:** `GET`
- **Path:** `/modules/:moduleId/aliases`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Get module version aliases](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Modules/getModuleVersionAliases)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleId` | path | `string` | yes | Module ID whose version aliases you want to retrieve. |
| `versionId` | query | `string` | no | Optionally filter aliases to a specific module version. |
