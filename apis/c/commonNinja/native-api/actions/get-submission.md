# Get Submission with Common Ninja

Retrieves a project submission from Common Ninja.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:projectId/submissions/:submissionId`
- **Base URL:** `https://api.commoninja.com/platform/api/v1`
- **Official documentation:** [Get Submission](https://developers.commoninja.com/docs/api/crm/submission)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `string` | yes | The project ID. |
| `submissionId` | path | `string` | yes | The submission ID. |
