# Update Job Application Comment with Polymer

Updates an existing job application comment in Polymer.

## Endpoint

- **Method:** `PUT`
- **Path:** `/job_applications/:job_application_id/comments/:comment_id`
- **Base URL:** `https://api.polymer.co/v1/hire`
- **Official documentation:** [Update Job Application Comment](https://developer.polymer.co/#update-a-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Updated comment HTML body. |
| `comment_id` | path | `string` | no | Numeric Polymer comment ID. |
| `job_application_id` | path | `string` | no | Numeric Polymer job application ID. |
