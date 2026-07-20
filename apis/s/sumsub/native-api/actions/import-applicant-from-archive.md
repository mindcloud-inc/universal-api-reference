# Import Applicant From Archive with Sumsub

## Endpoint

- **Method:** `POST`
- **Path:** `/resources/applicants/-/applicantImport`
- **Base URL:** `https://api.sumsub.com`
- **Official documentation:** [Import Applicant From Archive](https://docs.sumsub.com/reference/import-applicant-from-archive)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `archiveBase64` | body | `string` | yes | Base64-encoded zip archive containing applicant.json and applicantIdDoc.json plus the associated image files. |
