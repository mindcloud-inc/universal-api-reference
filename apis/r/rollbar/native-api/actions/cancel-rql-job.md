# Cancel RQL Job with Rollbar

Cancels an RQL job in Rollbar.

## Endpoint

- **Method:** `POST`
- **Path:** `/rql/job/:jobId/cancel`
- **Base URL:** `https://api.rollbar.com/api/1`
- **Official documentation:** [Cancel RQL Job](https://docs.rollbar.com/reference/cancel-an-rql-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `number` | yes | RQL job identifier |
