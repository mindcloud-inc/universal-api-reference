# Create Job with CATS

Creates a new job in CATS.

## Endpoint

- **Method:** `POST`
- **Path:** `/jobs`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Create Job](https://docs.catsone.com/api/v3/#jobs-create-a-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `check_duplicate` | query | `boolean` | no | If true, return an error instead of creating a duplicate job. |
| `title` | body | `string` | yes | The job title. |
| `company_id` | body | `number` | yes | The ID of the company the job belongs to. |
| `location.city` | body | `string` | yes | The job city. |
| `location.state` | body | `string` | yes | The job state. |
| `location.postal_code` | body | `string` | yes | The job postal code. |
