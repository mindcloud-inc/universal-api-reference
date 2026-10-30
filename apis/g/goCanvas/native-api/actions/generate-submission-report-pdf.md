# Generate Submission Report PDF with GoCanvas

## Endpoint

- **Method:** `GET`
- **Path:** `/submissions/:submissionId/reports/:reportId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Generate Submission Report PDF](https://api.gocanvas.com/api/v3/docs#generate-pdf-with-report-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submissionId` | path | `string` | yes | ID of the submission. |
| `reportId` | path | `string` | yes | ID of the report definition. |
