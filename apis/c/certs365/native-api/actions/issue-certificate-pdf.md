# Issue Certificate PDF with Certs 365

Creates a PDF certificate in Certs 365.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/issue-pdf`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Issue Certificate PDF](https://help.certs365.io/documentation/code-module-apis/issue-certification-pdf/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Issuer email. |
| `certificateNumber` | body | `string` | yes | Certificate number. |
| `name` | body | `string` | yes | Name associated with the certificate. |
| `course` | body | `string` | yes | Course name associated with the certificate. |
| `grantDate` | body | `date` | yes | Certificate grant date. |
| `expirationDate` | body | `date` | yes | Certificate expiration date. |
| `file` | body | `file` | yes | PDF file to upload. |
