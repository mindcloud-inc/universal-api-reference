# Create Applicant with Sumsub

## Endpoint

- **Method:** `POST`
- **Path:** `/resources/applicants`
- **Base URL:** `https://api.sumsub.com`
- **Official documentation:** [Create Applicant](https://docs.sumsub.com/reference/create-applicant)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `levelName` | query | `string` | yes | Verification level name configured in Sumsub. |
| `externalUserId` | body | `string` | yes | Unique applicant identifier on your side. |
