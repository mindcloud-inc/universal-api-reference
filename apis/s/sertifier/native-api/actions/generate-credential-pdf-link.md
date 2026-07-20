# Generate Credential PDF Link with Sertifier

Retrieves a credential PDF link from Sertifier.

## Endpoint

- **Method:** `GET`
- **Path:** `/credential/generatePDFLink/:credential_id_OR_certificate_no`
- **Base URL:** `https://b2b.sertifier.com`
- **Official documentation:** [Generate Credential PDF Link](https://sertifier.docs.apiary.io/reference/credential/generate-pdf-download-link-of-credential)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `credential_id_OR_certificate_no` | path | `string` | yes |
