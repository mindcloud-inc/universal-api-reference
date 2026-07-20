# List Tasks with bytebot

Retrieves a list of tasks from bytebot.

## Endpoint

- **Method:** `GET`
- **Path:** `{agentBaseUrl}/tasks`
- **Base URL:** `{agentBaseUrl}`
- **Official documentation:** [List Tasks](https://docs.bytebot.ai/api-reference/agent/tasks)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | no | Optional task status filter. Supported live values include PENDING, IN_PROGRESS, NEEDS_HELP, NEEDS_REVIEW, COMPLETED, CANCELLED, and FAILED. |
