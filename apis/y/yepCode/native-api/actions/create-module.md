# Create module with YepCode

Creates a new module in YepCode.

## Endpoint

- **Method:** `POST`
- **Path:** `/modules`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Create module](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Modules/createModule)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `programmingLanguage` | body | `string` | yes |
| `sourceCode` | body | `string` | yes |
