# List Tasks with LOBSTR.IO

Retrieves tasks from LOBSTR.IO.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/tasks`
- **Base URL:** `https://api.lobstr.io`
- **Official documentation:** [List Tasks](https://docs.lobstr.io/docs/list-tasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `squid` | query | `string` | yes | The squid hash ID to list tasks for. |
| `type` | query | `string` | no | Response detail level: url or params. |
