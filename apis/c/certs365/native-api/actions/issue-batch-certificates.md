# Issue Batch Certificates with Certs 365

Creates batch certificates in Certs 365 from Excel.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/batch-certificate-issue`
- **Base URL:** `https://api1.certs365.io`
- **Official documentation:** [Issue Batch Certificates](https://help.certs365.io/documentation/code-module-apis/issue-batch-certification-excel/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Issuer email. |
| `excelFile` | body | `file` | yes | Excel file containing the batch issue payload. |
