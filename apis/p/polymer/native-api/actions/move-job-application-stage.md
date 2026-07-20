# Move Job Application Stage with Polymer

Moves a job application to a hiring stage in Polymer.

## Endpoint

- **Method:** `POST`
- **Path:** `/job_applications/:job_application_id/move_stage`
- **Base URL:** `https://api.polymer.co/v1/hire`
- **Official documentation:** [Move Job Application Stage](https://developer.polymer.co/#move-stage)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hiring_stage_id` | body | `string` | no | Target hiring stage ID for the job application's job. |
| `job_application_id` | path | `string` | no | Numeric Polymer job application ID. |
| `skip_message_automations` | body | `string` | no | Whether to skip message automations on the target stage. Must be a boolean. |
