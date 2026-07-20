# Publish process version with YepCode

Creates a published process version in YepCode.

## Endpoint

- **Method:** `POST`
- **Path:** `/processes/:processId/versions`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Publish process version](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/publishProcessVersion)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `processId` | path | `string` | yes |
| `tag` | body | `string` | yes |
| `comment` | body | `string` | no |
