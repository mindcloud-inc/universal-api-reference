# List Projects with Crowdin

Retrieves projects from Crowdin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://api.crowdin.com/api/v2`
- **Official documentation:** [List Projects](https://support.crowdin.com/developer/api/v2/#operation/api.projects.getMany)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `orderBy` | query | `string` | no |
| `userId` | query | `number` | no |
| `hasManagerAccess` | query | `boolean` | no |
| `type` | query | `number` | no |
