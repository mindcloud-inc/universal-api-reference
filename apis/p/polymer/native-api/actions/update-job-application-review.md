# Update Job Application Review with Polymer

Updates an existing job application review in Polymer.

## Endpoint

- **Method:** `PUT`
- **Path:** `/job_applications/:job_application_id/reviews/:review_id`
- **Base URL:** `https://api.polymer.co/v1/hire`
- **Official documentation:** [Update Job Application Review](https://developer.polymer.co/#update-a-review)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Updated review HTML body. |
| `job_application_id` | path | `string` | no | Numeric Polymer job application ID. |
| `rating` | body | `string` | no | Updated review rating: strong_yes, weak_yes, weak_no, strong_no, or no_rating. |
| `review_id` | path | `string` | no | Numeric Polymer review ID. |
