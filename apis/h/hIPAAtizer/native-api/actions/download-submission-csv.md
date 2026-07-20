# Download Submission CSV with HIPAAtizer

Retrieves submission data as CSV from HIPAAtizer.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/api_key/submissions/:submissionId/csv`
- **Base URL:** `https://app.hipaatizer.com`
- **Official documentation:** [Download Submission CSV](https://github.com/HIPAAtizer/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submissionId` | path | `string` | yes | Submission identifier. |
