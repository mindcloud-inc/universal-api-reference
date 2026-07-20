# Get Compute Engine Task with SonarQube

Retrieves a compute engine task from SonarQube.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/ce/task`
- **Base URL:** `https://sonarcloud.io`
- **Official documentation:** [Get Compute Engine Task](https://sonarcloud.io/web_api/api/ce/task)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | Compute Engine task ID. Required by /api/ce/task. |
