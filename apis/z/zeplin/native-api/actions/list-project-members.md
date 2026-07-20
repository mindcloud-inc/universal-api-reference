# List Project Members with Zeplin

Retrieves a list of project members from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/members`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Project Members](https://docs.zeplin.dev/reference/getprojectmembers)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
