# List Project Pages with Zeplin

Retrieves a list of project pages from Zeplin.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{project_id}/pages`
- **Base URL:** `https://api.zeplin.dev/v1`
- **Official documentation:** [List Project Pages](https://docs.zeplin.dev/reference/getprojectpages)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Project id |
