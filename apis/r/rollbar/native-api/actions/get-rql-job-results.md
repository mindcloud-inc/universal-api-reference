# Get RQL Job Results with Rollbar

Retrieves RQL job results from Rollbar.

## Endpoint

- **Method:** `GET`
- **Path:** `/rql/job/:jobId/result`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Get RQL Job Results](https://docs.rollbar.com/reference/get-rql-job-results)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `number` | yes | RQL job identifier |
