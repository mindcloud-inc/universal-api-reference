# List Validation Jobs with Verifalia

Retrieves email validation jobs from Verifalia.

## Endpoint

- **Method:** `GET`
- **Path:** `/email-validations`
- **Base URL:** `https://api-1.verifalia.com/v2.7`
- **Official documentation:** [List Validation Jobs](https://verifalia.com/developers/email-verifications/listing-jobs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `createdOn` | query | `string` | no | Filter jobs created on one specific date in YYYY-MM-DD format. |
| `createdOn:since` | query | `string` | no | Inclusive start date for the job listing period in YYYY-MM-DD format. |
| `createdOn:until` | query | `string` | no | Inclusive end date for the job listing period in YYYY-MM-DD format. |
| `owner` | query | `string` | no | Only return jobs submitted by the specified Verifalia user ID. |
| `sort` | query | `string` | no | Sort jobs by `createdOn` or `-createdOn`. |
| `status` | query | `string` | no | One or more job statuses to include, separated by commas. |
| `status:exclude` | query | `string` | no | One or more job statuses to exclude, separated by commas. |
