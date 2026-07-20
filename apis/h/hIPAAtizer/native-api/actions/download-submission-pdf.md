# Download Submission PDF with HIPAAtizer

Retrieves a submission PDF from HIPAAtizer.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/api_key/submissions/:submissionId/pdf`
- **Base URL:** `https://app.hipaatizer.com`
- **Official documentation:** [Download Submission PDF](https://github.com/HIPAAtizer/api-docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submissionId` | path | `string` | yes | Submission identifier. |
| `fileOrder` | query | `number` | no | Optional file order index for PDF generation. |
