# Check Background Job Status with PDF.co

Retrieves a background job status from PDF.co.

## Endpoint

- **Method:** `GET`
- **Path:** `/job/check`
- **Base URL:** `https://api.pdf.co/v1`
- **Official documentation:** [Check Background Job Status](https://docs.pdf.co/api-reference/job-check)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jobid` | query | `string` | yes | Background job identifier returned by async PDF.co endpoints. |
