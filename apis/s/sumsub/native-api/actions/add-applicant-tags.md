# Add Applicant Tags with Sumsub

## Endpoint

- **Method:** `POST`
- **Path:** `/resources/applicants/:applicantId/tags/add`
- **Base URL:** `https://api.sumsub.com`
- **Official documentation:** [Add Applicant Tags](https://docs.sumsub.com/reference/add-custom-applicant-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `applicantId` | path | `string` | yes | Unique Sumsub applicant identifier. |
| `tags[]` | body | `array<string>` | yes | Tags to add to the applicant profile. |
