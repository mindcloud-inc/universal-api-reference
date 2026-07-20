# Import Job Application with Polymer

Imports a job application into Polymer.

## Endpoint

- **Method:** `POST`
- **Path:** `/job_applications/import`
- **Base URL:** `https://api.polymer.co/v1/hire`
- **Official documentation:** [Import Job Application](https://developer.polymer.co/#import-a-job-application)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | no | Candidate email address. |
| `first_name` | body | `string` | no | Candidate first name. |
| `job_id` | body | `string` | no | ID of the job to import into. |
