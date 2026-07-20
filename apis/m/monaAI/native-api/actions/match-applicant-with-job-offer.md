# Match Applicant With Job Offer with Mona AI

Matches an applicant with a job offer in Mona AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/matching/applicantWithJobOffer`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Match Applicant With Job Offer](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `applicantObject` | body | `object` | yes | Applicant object to match against a job offer. |
| `brandingInfo` | body | `object` | no | Optional branding information object. |
| `businessName` | body | `string` | no | Business name used for matching context. |
| `cvData` | body | `string` | no | CV data used for matching. |
| `jobOfferObject` | body | `object` | yes | Job offer object to match against the applicant. |
| `logs[]` | body | `array<object>` | no | Optional matching logs array. |
| `profileType` | body | `string` | no | Profile type used for matching context. |
| `profileURL` | body | `string` | no | Profile URL used for matching context. |
