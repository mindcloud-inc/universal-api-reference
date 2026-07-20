# Update Vacancy with Jaicob

## Endpoint

- **Method:** `PUT`
- **Path:** `/vacancies/[:id]`
- **Base URL:** `https://api.jaicob.ai`
- **Official documentation:** [Update Vacancy](https://developers.jaicob.ai/reference/update_vacancy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Vacancy identifier. |
| `title` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `yearsOfExperience` | body | `number` | no | — |
| `employmentType` | body | `string` | no | — |
| `workingHours` | body | `object` | no | — |
| `salary` | body | `object` | no | — |
| `location` | body | `object` | no | — |
| `tags[]` | body | `array<string>` | no | — |
| `userId` | body | `string` | no | — |
