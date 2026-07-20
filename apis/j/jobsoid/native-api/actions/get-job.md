# Get job with Jobsoid

Retrieves a published job from Jobsoid.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/jobs/{{jobId}}`
- **Base URL:** `https://demo.jobsoid.com`
- **Official documentation:** [Get job](https://apidocs.jobsoid.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `number` | yes | Unique Jobsoid job identifier from the jobs feed. |
