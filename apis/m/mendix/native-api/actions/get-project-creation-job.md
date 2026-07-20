# Get Project Creation Job with Mendix

Retrieves a project creation job status from Mendix.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/jobs/:jobId`
- **Base URL:** `https://projects-api.home.mendix.com/v2`
- **API:** rest
- **Official documentation:** [Get Project Creation Job](https://docs.mendix.com/apidocs-mxsdk/apidocs/projects-api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job-id` | path | `string` | yes | The unique identifier of a project creation job. |
