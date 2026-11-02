# List Time Tracking Project Tasks with BambooHR

Lists time tracking project tasks from BambooHR.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/time-tracking/projects/:projectId/tasks`
- **Base URL:** `https://{companyDomain}.bamboohr.com/api`
- **Official documentation:** [List Time Tracking Project Tasks](https://documentation.bamboohr.com/reference/list-project-tasks)

## Requirements

- **OAuth scopes:** `time_tracking:project`
- **scope:** `time_tracking:project` — BambooHR documents these OAuth scopes for this endpoint; access also follows the connected user permissions.

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | The project ID. |
| `filter` | query | `string` | no | OData v4 filter expression. Filterable fields: `id`, `name`, `projectId`, `billable`, `createdAt`, `updatedAt`, `deletedAt`. An explicit `deletedAt` predicate overrides the default `statuses[]=active` filter. |
| `sort` | query | `string` | no | Sort expression like `name asc, createdAt desc`. Allowed fields: `id`, `name`, `projectId`, `billable`, `createdAt`, `updatedAt`, `deletedAt`. |
| `statuses[]` | query | `list<string>` | no | Statuses to include. Defaults to `active` (excludes deleted tasks). Use both values to include active and deleted tasks. Accepted values: `active`, `deleted`. Send multiple values as a array. |
