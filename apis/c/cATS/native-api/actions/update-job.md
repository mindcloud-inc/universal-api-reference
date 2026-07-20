# Update Job with CATS

Updates an existing job in CATS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/jobs/:id`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Update Job](https://docs.catsone.com/api/v3/#jobs-update-a-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the job to update. |
| `title` | body | `string` | yes | The job title. |
| `company_id` | body | `number` | yes | The ID of the company the job belongs to. |
| `location.city` | body | `string` | yes | The job city. |
| `location.state` | body | `string` | yes | The job state. |
| `location.postal_code` | body | `string` | yes | The job postal code. |
