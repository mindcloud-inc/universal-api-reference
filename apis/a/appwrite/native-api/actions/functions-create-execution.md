# Create execution with Appwrite

Creates a new execution in your Appwrite project.

## Endpoint

- **Method:** `POST`
- **Path:** `/functions/{functionId}/executions`
- **Base URL:** `https://cloud.appwrite.io/v1`
- **Official documentation:** [Create execution](https://appwrite.io/docs/references/cloud/server-rest/functions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `functionId` | path | `string` | yes | Function ID. |
| `body` | body | `string` | no | HTTP body of execution. Default value is empty string. |
| `async` | body | `boolean` | no | Execute code in the background. Default value is false. |
| `path` | body | `string` | no | HTTP path of execution. Path can include query params. Default value is / |
| `method` | body | `string` | no | HTTP method of execution. Default value is POST. |
| `headers` | body | `object` | no | HTTP headers of execution. Defaults to empty. |
| `scheduledAt` | body | `string` | no | Scheduled execution time in [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html) format. DateTime value must be in future with precision in minutes. |
