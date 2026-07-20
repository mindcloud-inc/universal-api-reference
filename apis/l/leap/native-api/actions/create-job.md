# Create Job with Leap

Creates a new job in Leap.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs`
- **Base URL:** `https://api.jobprogress.com/api/v3`
- **Official documentation:** [Create Job](https://docs.api.jobprogress.com/api/job.json)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | Street address for the job when not using the customer address. |
| `city` | body | `string` | no | City for the job address. |
| `country_id` | body | `number` | no | Country ID for the job address. |
| `customer_id` | body | `number` | yes | Leap customer ID associated with the job. |
| `description` | body | `string` | yes | Description of the job. |
| `name` | body | `string` | no | Optional name for the job. |
| `same_as_customer_address` | body | `number` | no | Set to 1 to reuse the customer address, or 0 to provide a job-specific address. |
| `state_id` | body | `number` | no | State ID for the job address. |
| `trade_0_id` | body | `number` | yes | Trade ID to associate with the job. |
| `zip` | body | `number` | no | ZIP or postal code for the job address. |
