# Set Submission Refill Link with Youform

Enables or disables a submission refill link in Youform.

## Endpoint

- **Method:** `POST`
- **Path:** `/submissions/:submissionId/refill-link`
- **Base URL:** `https://app.youform.com/api`
- **Official documentation:** [Set Submission Refill Link](https://youform.com/api-docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submissionId` | path | `number` | yes | Numeric ID of the submission whose refill link you want to enable or disable. |
| `enable` | body | `boolean` | yes | Set to true to enable the refill link or false to disable it. |
