# Get Submission with MoreApp

Retrieves a submission from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/customers/{{customerId}}/submissions/{{submissionId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Get Submission](https://docs.moreapp.com/docs/developer-docs/42c8ecbd569f3-get-a-single-submission)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | MoreApp customer identifier. |
| `submissionId` | path | `string` | yes | MoreApp submission identifier. |
