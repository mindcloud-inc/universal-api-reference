# List Testdriver Results with Dashcam

Retrieves TestDriver test results from Dashcam.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/testdriver-results`
- **Base URL:** `https://api.testdriver.ai`
- **Official documentation:** [List Testdriver Results](https://docs.testdriver.ai/v6/getting-started/ci)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `branch` | query | `string` | no |
| `page` | query | `string` | no |
| `repo` | query | `string` | no |
