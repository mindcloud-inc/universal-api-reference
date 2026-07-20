# Get All Tasks with Mews

Retrieves tasks from Mews.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/getAll`
- **Base URL:** `{platformAddress}/api/connector/v1`
- **Official documentation:** [Get All Tasks](https://github.com/MewsSystems/gitbook-connector-api/blob/master/operations/tasks.md#get-all-tasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `TaskIds[]` | body | `array<string>` | no | Optional task identifiers to fetch specific tasks. |
