# Delete Job Application Comment with Polymer

Deletes an existing job application comment from Polymer.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/job_applications/:job_application_id/comments/:comment_id`
- **Base URL:** `https://api.polymer.co/v1/hire`
- **Official documentation:** [Delete Job Application Comment](https://developer.polymer.co/#delete-a-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `comment_id` | path | `string` | no | Numeric Polymer comment ID. |
| `job_application_id` | path | `string` | no | Numeric Polymer job application ID. |
