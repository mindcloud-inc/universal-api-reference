# Add Applicant Note with Sumsub

## Endpoint

- **Method:** `POST`
- **Path:** `/resources/api/applicants/notes`
- **Base URL:** `https://api.sumsub.com`
- **Official documentation:** [Add Applicant Note](https://docs.sumsub.com/reference/add-applicant-note)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `applicantId` | body | `string` | yes | Unique Sumsub applicant identifier. |
| `note` | body | `string` | yes | Text of the note to add to the applicant profile. |
| `tags[]` | body | `array<string>` | no | Optional tags to associate with the note. |
