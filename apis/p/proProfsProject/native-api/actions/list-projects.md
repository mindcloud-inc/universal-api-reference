# List Projects with ProProfs Project

Retrieves a list of projects from ProProfs Project.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://api.projectbubble.com/v2`
- **Official documentation:** [List Projects](https://help.proprofsproject.com/projects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_id` | query | `string` | no | Filter projects by client ID. |
| `limit` | query | `string` | no | Maximum number of records to return. |
| `offset` | query | `string` | no | Start position for fetching records. |
| `order` | query | `string` | no | Sort order. Valid values: projectname, duedate, progress, billablehours, latest. |
| `status` | query | `string` | no | Filter projects by status. |
