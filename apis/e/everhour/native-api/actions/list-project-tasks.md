# List Project Tasks with Everhour

Retrieves tasks for a project from Everhour.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/tasks`
- **Base URL:** `https://api.everhour.com`
- **Official documentation:** [List Project Tasks](https://everhour.docs.apiary.io/)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `limit` | query | `number` | no | Maximum number of records to return. |
| `page` | query | `number` | no | Page number to return. |
| `projectId` | path | `string` | yes | Everhour project ID. |
| `query` | query | `string` | no | Filter tasks by name or search term. |
