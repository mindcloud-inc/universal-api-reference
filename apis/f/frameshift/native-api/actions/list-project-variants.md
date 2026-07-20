# List Project Variants with Frameshift

Retrieves a list of project variants from Frameshift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/variants/list`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [List Project Variants](https://mosaic.frameshift.io/api/#api-Variants-GetProjectVariantsList)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Resource identifier for the project to access |
| `search` | query | `string` | no | The search keyword to filter the results by |
