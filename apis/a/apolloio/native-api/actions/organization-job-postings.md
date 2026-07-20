# Organization Job Postings with Apollo

Retrieves organization job postings from Apollo.

## Endpoint

- **Method:** `GET`
- **Path:** `v1/organizations/:organization_id/job_postings`
- **Base URL:** `https://app.apollo.io/api`
- **Official documentation:** [Organization Job Postings](https://docs.apollo.io/reference/organization-jobs-postings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | path | `string` | yes | The organization ID of the company for which you want to find job postings. Each company in the Apollo database is assigned a unique ID. To find IDs, call the Organization Search endpoint and identify the values for `organization_id`. Example: `5e66b6381e05b4008c8331b8` |
