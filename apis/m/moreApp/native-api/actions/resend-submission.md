# Resend Submission with MoreApp

Resends a submission in MoreApp.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1.0/customers/{{customerId}}/submissions/resend/{{submissionId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Resend Submission](https://docs.moreapp.com/docs/developer-docs/1df53b019ea65-resend-a-submission)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `submissionId` | path | `string` | yes |
