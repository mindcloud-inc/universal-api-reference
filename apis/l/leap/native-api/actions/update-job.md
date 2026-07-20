# Update Job with Leap

Updates an existing job in Leap.

## Endpoint

- **Method:** `PUT`
- **Path:** `/jobs/[:jobId]`
- **Base URL:** `https://api.jobprogress.com/api/v3`
- **Official documentation:** [Update Job](https://docs.api.jobprogress.com/api/job.json)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_city` | body | `string` | no | City for the job address. |
| `address_country_id` | body | `number` | no | Country ID for the job address. |
| `address_state_id` | body | `number` | no | State ID for the job address. |
| `address_street` | body | `string` | no | Street address for the job when not using the customer address. |
| `address_zip` | body | `number` | no | ZIP or postal code for the job address. |
| `customer_id` | body | `number` | yes | Leap customer ID associated with the job. |
| `description` | body | `string` | yes | Description of the job. |
| `jobId` | path | `number` | yes | Leap job ID. |
| `name` | body | `string` | no | Optional name for the job. |
| `same_as_customer_address` | body | `number` | no | Set to 1 to reuse the customer address, or 0 to provide a job-specific address. |
| `trade_0_id` | body | `number` | yes | Trade ID to associate with the job. |
