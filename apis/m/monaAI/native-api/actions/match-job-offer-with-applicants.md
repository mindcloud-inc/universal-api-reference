# Match Job Offer With Applicants with Mona AI

Matches a job offer with applicants in Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/matching/jobOfferWithMultipleApplicants`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Match Job Offer With Applicants](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `applicantObjects[]` | body | `array<object>` | yes | Applicant objects to match against the job offer. |
| `brandingInfo` | body | `object` | no | Optional branding information object. |
| `businessName` | body | `string` | no | Business name used for matching context. |
| `cvData` | body | `string` | no | CV data used for matching. |
| `jobOfferObject` | body | `object` | yes | Job offer object to match against multiple applicants. |
| `logs[]` | body | `array<object>` | no | Optional matching logs array. |
| `profileType` | body | `string` | no | Profile type used for matching context. |
| `profileURL` | body | `string` | no | Profile URL used for matching context. |
