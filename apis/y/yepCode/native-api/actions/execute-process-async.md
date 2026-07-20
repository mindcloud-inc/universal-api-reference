# Execute process async with YepCode

Creates an asynchronous process execution in YepCode.

## Endpoint

- **Method:** `POST`
- **Path:** `/processes/:identifier/execute`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Execute process async](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/executeProcessAsync)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `identifier` | path | `string` | yes |
| `parameters` | body | `string` | yes |
| `comment` | body | `string` | no |
