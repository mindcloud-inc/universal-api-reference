# List Projects with WebWork Time Tracker

Retrieves workspace projects from WebWork Time Tracker.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://api.webwork-tracker.com/api/v2`
- **Official documentation:** [List Projects](https://api-docs.webwork-tracker.com/api/projects/getprojects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspace_id` | query | `number` | yes |
| `name` | query | `string` | no |
