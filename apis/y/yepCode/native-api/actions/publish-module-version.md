# Publish module version with YepCode

Creates a published module version in YepCode.

## Endpoint

- **Method:** `POST`
- **Path:** `/modules/:moduleId/versions`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Publish module version](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Modules/publishModuleVersion)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `moduleId` | path | `string` | yes |
| `tag` | body | `string` | yes |
| `comment` | body | `string` | no |
