# List Jobs with Connecteam

Get a list of job objects relevant to instance id (scheduler id or time clock id).
If unified jobs are disabled, only schedulers are supported

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/v1/jobs`
- **Base URL:** `https://api.connecteam.com`
- **Official documentation:** [List Jobs](https://developer.connecteam.com/reference/get_jobs_jobs_v1_jobs_get)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `instanceIds` | query | `array<number>` | no | Send multiple values as a array. |
| `jobIds` | query | `array<string>` | no | Send multiple values as a array. |
| `jobNames` | query | `array<string>` | no | Send multiple values as a array. |
| `jobCodes` | query | `array<string>` | no | Send multiple values as a array. |
| `includeDeleted` | query | `boolean` | no | — |
| `sort` | query | `string` | no | — |
| `order` | query | `string` | no | — |
| `limit` | query | `number` | no | — |
| `offset` | query | `number` | no | — |
