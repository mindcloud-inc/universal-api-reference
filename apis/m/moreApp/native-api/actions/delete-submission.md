# Delete Submission with MoreApp

Deletes a submission from MoreApp.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1.0/customers/{{customerId}}/submissions/{{submissionId}}`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Delete Submission](https://docs.moreapp.com/docs/developer-docs/b9bd9cc2b74ef-delete-a-submission)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `submissionId` | path | `string` | yes |
| `timestamp` | query | `number` | no |
