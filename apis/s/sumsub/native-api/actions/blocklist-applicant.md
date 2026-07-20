# Blocklist Applicant with Sumsub

## Endpoint

- **Method:** `POST`
- **Path:** `/resources/applicants/:applicantId/blacklist`
- **Base URL:** `https://api.sumsub.com`
- **Official documentation:** [Blocklist Applicant](https://docs.sumsub.com/reference/add-applicant-to-blocklist)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `applicantId` | path | `string` | yes | — |
| `note` | query | `string` | yes | Reason for blocklisting the applicant. |
