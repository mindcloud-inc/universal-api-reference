# Create Candidate with Jaicob

## Endpoint

- **Method:** `POST`
- **Path:** `/candidates`
- **Base URL:** `https://api.jaicob.ai`
- **Official documentation:** [Create Candidate](https://developers.jaicob.ai/reference/create_candidate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `applicantDetails` | body | `object` | yes | Candidate identity and contact details. |
| `status` | body | `string` | no | — |
| `function` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `tags[]` | body | `array<string>` | no | — |
| `linkedInSlug` | body | `string` | no | — |
| `languages[]` | body | `array<object>` | no | — |
| `skills[]` | body | `array<object>` | no | — |
| `workExperiences[]` | body | `array<object>` | no | — |
| `educations[]` | body | `array<object>` | no | — |
| `certifications[]` | body | `array<object>` | no | — |
| `locationIds[]` | body | `array<string>` | no | — |
