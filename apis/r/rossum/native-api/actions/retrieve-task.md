# Retrieve Task with Rossum

Retrieves a task from Rossum.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:taskID`
- **Base URL:** `https://mindcloud.rossum.app/api/v1`
- **Official documentation:** [Retrieve Task](https://rossum.app/api/docs/openapi/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskID` | path | `number` | yes | Rossum task ID. |
| `no_redirect` | query | `boolean` | no | When true, return the task resource instead of redirecting. |
