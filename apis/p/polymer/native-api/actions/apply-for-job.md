# Apply For Job with Polymer

Applies a candidate to a job in Polymer.

## Endpoint

- **Method:** `POST`
- **Path:** `/job_applications/apply`
- **Base URL:** `https://api.polymer.co/v1/hire`
- **Official documentation:** [Apply For Job](https://developer.polymer.co/#apply-for-a-job)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Candidate email address. |
| `first_name` | body | `string` | no | Candidate first name. |
| `job_id` | body | `string` | no | ID of the job to apply to. |
| `send_candidate_confirmation_email` | body | `string` | no | Whether Polymer should send a candidate confirmation email. Must be a boolean. |
