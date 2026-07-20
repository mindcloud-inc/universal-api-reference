# Update Candidate with Jaicob

## Endpoint

- **Method:** `PUT`
- **Path:** `/candidates/[:id]`
- **Base URL:** `https://api.jaicob.ai`
- **Official documentation:** [Update Candidate](https://developers.jaicob.ai/reference/update_candidate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Candidate identifier. |
| `applicantDetails` | body | `object` | no | Candidate identity and contact details. |
| `userId` | body | `string` | no | — |
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
