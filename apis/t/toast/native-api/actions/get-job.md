# Get Job with Toast

Retrieves one labor job by Toast GUID or external identifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/labor/v1/jobs/:jobId`
- **Base URL:** `{connection}`
- **API:** Labor
- **Official documentation:** [Get Job](https://doc.toasttab.com/openapi/labor/operation/jobsJobIdGet/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | The Toast GUID or external identifier of the job. |
