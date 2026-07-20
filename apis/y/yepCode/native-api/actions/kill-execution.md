# Kill execution with YepCode

Updates an execution in YepCode by terminating it.

## Endpoint

- **Method:** `PUT`
- **Path:** `/executions/:id/kill`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Kill execution](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Executions/killExecution)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the execution to terminate. |
