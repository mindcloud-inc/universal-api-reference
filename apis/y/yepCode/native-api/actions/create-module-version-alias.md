# Create module version alias with YepCode

Creates a module version alias in YepCode.

## Endpoint

- **Method:** `POST`
- **Path:** `/modules/:moduleId/aliases`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Create module version alias](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Modules/createModuleVersionAlias)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `moduleId` | path | `string` | yes |
| `name` | body | `string` | yes |
| `versionId` | body | `string` | yes |
