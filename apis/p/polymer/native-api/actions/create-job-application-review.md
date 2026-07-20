# Create Job Application Review with Polymer

Creates a review for a job application in Polymer.

## Endpoint

- **Method:** `POST`
- **Path:** `/job_applications/:job_application_id/reviews`
- **Base URL:** `https://api.polymer.co/v1/hire`
- **Official documentation:** [Create Job Application Review](https://developer.polymer.co/#create-a-review)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Review HTML body. |
| `job_application_id` | path | `string` | no | Numeric Polymer job application ID. |
| `rating` | body | `string` | no | Review rating: strong_yes, weak_yes, weak_no, strong_no, or no_rating. |
