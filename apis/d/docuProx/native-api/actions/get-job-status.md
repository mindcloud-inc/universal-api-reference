# Get Job Status with DocuProx

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/job-status`
- **Base URL:** `https://api.docuprox.com`
- **Official documentation:** [Get Job Status](https://docuprox.com/docs/api/#job-status-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_id` | query | `string` | yes | UUID of the asynchronous DocuProx job to inspect. |
