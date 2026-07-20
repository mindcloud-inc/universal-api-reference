# List Projects with FreeAgent

Retrieves a list of projects from FreeAgent.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://api.freeagent.com/v2`
- **Official documentation:** [List Projects](https://dev.freeagent.com/docs/projects#list-all-projects)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact` | query | `string` | no | Filter projects by FreeAgent contact resource URL. |
| `view` | query | `string` | no | Filter the project collection by FreeAgent view. |
