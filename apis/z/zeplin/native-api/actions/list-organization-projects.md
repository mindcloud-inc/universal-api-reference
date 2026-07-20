# List Organization Projects with Zeplin

Retrieves a list of organization projects from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/{organization_id}/projects`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Organization Projects](https://docs.zeplin.dev/reference/getorganizationprojects)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | path | `string` | yes | Organization id |
