# List Tasks with Nozbe Personal

Retrieves accessible tasks from Nozbe Personal.

## Endpoint

- **Method:** `GET`
- **Path:** `/tasks`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [List Tasks](https://api4.nozbe.com/v1/api#/tasks/getTasks)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | query | `string` | no | Filter tasks by project. |
| `sortBy` | query | `string` | no | Comma-separated sort expression. |
| `fields` | query | `string` | no | Comma-separated list of fields to return. |
