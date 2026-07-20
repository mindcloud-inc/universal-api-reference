# Edit Applicant Note with Sumsub

## Endpoint

- **Method:** `PATCH`
- **Path:** `/resources/api/applicants/notes`
- **Base URL:** `https://api.sumsub.com`
- **Official documentation:** [Edit Applicant Note](https://docs.sumsub.com/reference/edit-applicant-note)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `string` | yes |
| `applicantId` | body | `string` | yes |
| `note` | body | `string` | yes |
| `tags[]` | body | `array<string>` | no |
