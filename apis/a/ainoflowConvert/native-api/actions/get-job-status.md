# Get Job Status with Ainoflow Convert

Retrieves conversion job status and download URLs from Ainoflow Convert.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/convert/jobs/:jobId`
- **Base URL:** `https://api.ainoflow.io`
- **Official documentation:** [Get Job Status](https://www.ainoflow.io/docs/api/convert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobId` | path | `string` | yes | Job ID returned from a submit action. |
