# Approve Applicant with Sumsub

## Endpoint

- **Method:** `POST`
- **Path:** `/resources/applicants/:applicantId/-/approve`
- **Base URL:** `https://api.sumsub.com`
- **Official documentation:** [Approve Applicant](https://docs.sumsub.com/reference/approve-applicant)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `applicantId` | path | `string` | yes |
| `note` | body | `string` | no |
| `tags[]` | body | `array<string>` | no |
