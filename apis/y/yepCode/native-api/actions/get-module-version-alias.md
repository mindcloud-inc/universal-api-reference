# Get module version alias with YepCode

Retrieves a module version alias from YepCode.

## Endpoint

- **Method:** `GET`
- **Path:** `/modules/:moduleId/aliases/:aliasId`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Get module version alias](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Modules/getModuleVersionAlias)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `moduleId` | path | `string` | yes | Module ID whose alias you want to retrieve. |
| `aliasId` | path | `string` | yes | Alias ID to retrieve. |
