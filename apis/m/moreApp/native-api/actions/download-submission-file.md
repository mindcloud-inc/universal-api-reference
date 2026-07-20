# Download Submission File with MoreApp

Downloads a submission file from MoreApp.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1.0/customers/{{customerId}}/registrationFile/{{fileId}}/download`
- **Base URL:** `https://api.moreapp.com`
- **Official documentation:** [Download Submission File](https://docs.moreapp.com/docs/developer-docs/ce7e32b88411a-download-submission-file)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customerId` | path | `number` | yes |
| `fileId` | path | `string` | yes |
