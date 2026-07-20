# Create process version alias with YepCode

Creates a process version alias in YepCode.

## Endpoint

- **Method:** `POST`
- **Path:** `/processes/:processId/aliases`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Create process version alias](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/createProcessVersionAlias)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `processId` | path | `string` | yes |
| `name` | body | `string` | yes |
| `versionId` | body | `string` | yes |
