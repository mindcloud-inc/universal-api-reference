# Check RQL Job with Rollbar

Retrieves an RQL job from Rollbar.

## Endpoint

- **Method:** `GET`
- **Path:** `/rql/job/:jobId`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Check RQL Job](https://docs.rollbar.com/reference/get-an-rql-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `number` | yes | RQL job identifier |
