# List Applications with Recooty

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/jobs/{{jobId}}/applications`
- **Base URL:** `https://standaloneapi.recooty.app/api`
- **Official documentation:** [List Applications](https://api.recooty.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The Recooty job ID. |
| `page` | query | `string` | no | The page number to retrieve. |
