# Create process with YepCode

Creates a new process in YepCode.

## Endpoint

- **Method:** `POST`
- **Path:** `/processes`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Create process](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/createProcess)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `slug` | body | `string` | yes |
| `programmingLanguage` | body | `string` | yes |
| `sourceCode` | body | `string` | yes |
| `parametersSchema` | body | `string` | yes |
