# List All Sample Files with Frameshift

Retrieves all sample files from Frameshift.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/projects/:project_id/samples/files`
- **Base URL:** `https://mosaic.frameshift.io/api`
- **Official documentation:** [List All Sample Files](https://mosaic.frameshift.io/api/#api-Sample_Files-Get_All_Sample_Files)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_id` | path | `string` | yes | Resource identifier for the project to access |
| `search` | query | `string` | no | The search keyword to filter the results by |
