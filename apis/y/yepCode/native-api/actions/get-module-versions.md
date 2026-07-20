# Get module versions with YepCode

Retrieves module version records from YepCode.

## Endpoint

- **Method:** `GET`
- **Path:** `/modules/:moduleId/versions`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Get module versions](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Modules/getModuleVersions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleId` | path | `string` | yes | Unique identifier of the module whose versions you want to retrieve. |
