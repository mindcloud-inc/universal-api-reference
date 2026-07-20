# Download Submission Log with HIPAAtizer

Retrieves submission access logs from HIPAAtizer.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/api_key/submissions/:submissionId/logs`
- **Base URL:** `https://app.hipaatizer.com`
- **Official documentation:** [Download Submission Log](https://github.com/HIPAAtizer/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submissionId` | path | `string` | yes | Submission identifier. |
