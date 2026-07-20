# List Task Comments with actiTIME

Retrieves comments for a task in actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks/:id/comments`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [List Task Comments](https://www.actitime.com/api-documentation/tasks-resource)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Task identifier. |
| `includeReferenced` | query | `string` | no | Comma-separated referenced objects to include. |
