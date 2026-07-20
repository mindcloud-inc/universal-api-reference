# Create Job Application Comment with Polymer

Creates a comment for a job application in Polymer.

## Endpoint

- **Method:** `POST`
- **Path:** `/job_applications/:job_application_id/comments`
- **Base URL:** `https://api.polymer.co/v1/hire`
- **Official documentation:** [Create Job Application Comment](https://developer.polymer.co/#create-a-comment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | no | Comment HTML body. Plain text is automatically wrapped by Polymer. |
| `job_application_id` | path | `string` | no | Numeric Polymer job application ID. |
