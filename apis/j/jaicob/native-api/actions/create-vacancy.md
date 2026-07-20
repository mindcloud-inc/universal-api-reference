# Create Vacancy with Jaicob

## Endpoint

- **Method:** `POST`
- **Path:** `/vacancies`
- **Base URL:** `https://api.jaicob.ai`
- **Official documentation:** [Create Vacancy](https://developers.jaicob.ai/reference/create_vacancy)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `title` | body | `string` | yes |
| `description` | body | `string` | yes |
| `yearsOfExperience` | body | `number` | yes |
| `employmentType` | body | `string` | no |
| `workingHours` | body | `object` | yes |
| `salary` | body | `object` | yes |
| `location` | body | `object` | yes |
| `tags[]` | body | `array<string>` | no |
| `locationIds[]` | body | `array<string>` | no |
| `educationLevelId` | body | `number` | yes |
| `seniorityId` | body | `number` | yes |
| `industryId` | body | `number` | yes |
| `jobCategoryId` | body | `number` | yes |
| `bannerImage` | body | `string` | no |
