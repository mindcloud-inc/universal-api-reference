# Get Rejected Records For Submission with ZAP POST

Retrieves rejected records for a specific submission from ZAP POST.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/RejectedRecords/:submissionId`
- **Base URL:** `https://api.zappost.com`
- **Official documentation:** [Get Rejected Records For Submission](https://apidocumentation.zappost.com/api-endpoints/rejectedrecords)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submissionId` | path | `string` | yes | The submission UUID to inspect rejected records for. |
