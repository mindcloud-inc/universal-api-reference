# Batch Delete Scripts with Dremio

Deletes scripts from a Dremio project in batch.

## Endpoint

- **Method:** `POST`
- **Path:** `/projects/:project_id/scripts:batchDelete`
- **Base URL:** `https://api.dremio.cloud/v0`
- **Official documentation:** [Batch Delete Scripts](https://docs.dremio.com/dremio-cloud/api/scripts/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `ids` | body | `list<string>` | yes |
| `project_id` | path | `string` | yes |
