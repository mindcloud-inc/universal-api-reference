# Get Job Status with Diabolocom

Retrieves a task job status from Diabolocom.

## Endpoint

- **Method:** `GET`
- **Path:** `https://execute.diabolocom.ai/api/job/status/:jobId`
- **Base URL:** `https://api.diabolocom.ai`
- **Official documentation:** [Get Job Status](https://developer.diabolocom.com/api/collections/6612236/S1EKzfUU?segregateAuth=true&versionTag=latest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The Diabolocom job ID returned when a text or audio task was submitted. |
| `expires` | query | `string` | yes | Temporary expiry value from the job_status_endpoint_url returned by a Diabolocom job creation response. |
| `signature` | query | `string` | yes | Temporary signature value from the job_status_endpoint_url returned by a Diabolocom job creation response. |
