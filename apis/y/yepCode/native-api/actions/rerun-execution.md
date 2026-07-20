# Rerun execution with YepCode

Creates a new execution in YepCode from an existing one.

## Endpoint

- **Method:** `POST`
- **Path:** `/executions/:id/rerun`
- **Base URL:** `https://cloud.yepcode.io/api/{team}/rest`
- **Official documentation:** [Rerun execution](https://cloud.yepcode.io/api/rest/public/swagger-ui/index.html#/Executions/rerunExecution)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier of the execution to rerun. |
