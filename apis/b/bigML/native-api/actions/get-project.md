# Get Project with BigML

Retrieves a project from BigML.

## Endpoint

- **Method:** `GET`
- **Path:** `/project/:projectId`
- **Base URL:** `https://bigml.io`
- **Official documentation:** [Get Project](https://bigml.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | BigML project identifier suffix only (for example, 69cd1234abcd1234abcd1234). Do not include project/. |
