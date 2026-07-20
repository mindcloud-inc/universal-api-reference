# Delete Job Application Review with Polymer

Deletes an existing job application review from Polymer.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/job_applications/:job_application_id/reviews/:review_id`
- **Base URL:** `https://api.polymer.co/v1/hire`
- **Official documentation:** [Delete Job Application Review](https://developer.polymer.co/#delete-a-review)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `job_application_id` | path | `string` | no | Numeric Polymer job application ID. |
| `review_id` | path | `string` | no | Numeric Polymer review ID. |
