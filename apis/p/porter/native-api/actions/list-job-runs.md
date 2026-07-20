# List Job Runs with Porter

Retrieves job runs from a Porter project.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v2/projects/:projectId/job_runs`
- **Base URL:** `https://dashboard.porter.run`
- **Official documentation:** [List Job Runs](https://docs.porter.run/applications/configuration-as-code/services/job-service)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The Porter project ID whose job runs you want to list. |
