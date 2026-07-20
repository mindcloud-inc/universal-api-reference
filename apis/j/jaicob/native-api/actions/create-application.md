# Create Application with Jaicob

## Endpoint

- **Method:** `POST`
- **Path:** `/applications/[:vacancyId]`
- **Base URL:** `https://api.jaicob.ai`
- **Official documentation:** [Create Application](https://developers.jaicob.ai/reference/create_application)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `vacancyId` | path | `string` | yes | Vacancy identifier. |
| `applicantDetails` | body | `object` | yes | Applicant identity and contact details. |
| `function` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `resumeUrl` | body | `string` | no | — |
| `workExperiences[]` | body | `array<object>` | no | — |
| `educations[]` | body | `array<object>` | no | — |
| `certifications[]` | body | `array<object>` | no | — |
| `appliedWith` | body | `string` | no | — |
| `coverLetter` | body | `string` | no | — |
| `remarks` | body | `string` | no | — |
