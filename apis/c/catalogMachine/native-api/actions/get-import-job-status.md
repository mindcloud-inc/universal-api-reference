# Get Import Job Status with Catalog Machine

Retrieves import job status from Catalog Machine.

## Endpoint

- **Method:** `GET`
- **Path:** `/jobs/import/:jobId`
- **Base URL:** `https://www.catalogmachine.com/api/v1`
- **Official documentation:** [Get Import Job Status](https://help.catalogmachine.com/en/articles/3667421-rest-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Import job id returned by start import actions. |
