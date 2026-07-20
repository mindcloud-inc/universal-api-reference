# Schedule process with YepCode

Creates a scheduled process in YepCode.

## Endpoint

- **Method:** `POST`
- **Path:** `/processes/:identifier/schedule`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Schedule process](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Processes/createSchedule)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `identifier` | path | `string` | yes |
| `cron` | body | `string` | no |
| `allowConcurrentExecutions` | body | `boolean` | no |
| `dateTime` | body | `string` | no |
| `input.parameters` | body | `string` | no |
| `input.comment` | body | `string` | no |
