# List Project Activities with Frameshift

Retrieves a list of project activities from Frameshift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/activities`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [List Project Activities](https://mosaic.frameshift.io/api/#api-Activities-GetActivities)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `project_id` | path | `number` | yes |
