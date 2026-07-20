# List Projects with Nozbe Personal

Retrieves accessible projects from Nozbe Personal.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://api4.nozbe.com/v1/api`
- **Official documentation:** [List Projects](https://api4.nozbe.com/v1/api#/projects/getProjects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sortBy` | query | `string` | no | Comma-separated sort expression. |
| `team_id` | query | `string` | no | Filter projects by team. |
| `is_single_actions` | query | `boolean` | no | Filter by single-task projects. |
