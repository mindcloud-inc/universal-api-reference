# Upload Remote Workflows with Shuffler

Uploads remote workflows to Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows/download_remote`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Upload Remote Workflows](https://shuffler.io/docs/API#upload-a-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `branch` | body | `string` | no | Git branch. |
| `password` | body | `string` | no | Git password or PAT. |
| `url` | body | `string` | yes | Workflow file or repository URL. |
| `username` | body | `string` | no | Git username. |
