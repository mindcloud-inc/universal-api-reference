# <img src="https://images.mindcloud.co/apps/icons/certs365_1774886846028.png" alt="Certs 365 logo" width="28" height="28"> Certs 365: Universal API

Digital credential issuance, certificate lifecycle, issuer management, storage, and blockchain verification APIs for Certs 365.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/certs365/latest
- **Category:** Human Resources / Learning (LMS)
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://certs365.io
- **Vendor API docs:** https://help.certs365.io/documentation/api-endpoints/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Issuers](actions/list-issuers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/certs365/latest/actions/list-issuers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Balance

| Action | Method | Description |
| --- | --- | --- |
| [Check Balance](actions/check-balance.md) | GET | Retrieves the MATIC balance from Certs 365. |

### Batchcertificate

| Action | Method | Description |
| --- | --- | --- |
| [Get Batch Certificates](actions/get-batch-certificates.md) | GET | Retrieves batch certificates from Certs 365 storage. |
| [Issue Batch Certificates](actions/issue-batch-certificates.md) | POST | Creates batch certificates in Certs 365 from Excel. |
| [Renew Batch](actions/renew-batch.md) | PUT | Updates batch certificate expirations in Certs 365. |
| [Update Batch Status](actions/update-batch-status.md) | PUT | Updates batch certificate statuses in Certs 365. |

### Certificate

| Action | Method | Description |
| --- | --- | --- |
| [Find Certificate](actions/find-certificate.md) | GET | Finds a certificate in Certs 365 by ID or name. |
| [Get Organization Issues](actions/get-organization-issues.md) | GET | Retrieves organization-issued certificates from Certs 365. |
| [Get Single Certificates](actions/get-single-certificates.md) | GET | Retrieves single certificates from Certs 365 storage. |
| [Issue Certificate](actions/issue-certificate.md) | POST | Creates a certificate in Certs 365. |
| [Issue Certificate PDF](actions/issue-certificate-pdf.md) | POST | Creates a PDF certificate in Certs 365. |
| [Renew Certificate](actions/renew-certificate.md) | PUT | Updates a certificate expiration in Certs 365. |
| [Update Certificate Status](actions/update-certificate-status.md) | PUT | Updates a certificate status in Certs 365. |

### Certificateasset

| Action | Method | Description |
| --- | --- | --- |
| [Upload Certificate Asset](actions/upload-certificate-asset.md) | POST | Uploads a certificate asset to Certs 365 storage. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Upload Media File](actions/upload-media-file.md) | POST | Uploads a media file to Certs 365 storage. |

### Graphdata

| Action | Method | Description |
| --- | --- | --- |
| [Get Status Graph Data](actions/get-status-graph-data.md) | GET | Retrieves monthly status graph data from Certs 365. |
| [Get Yearly Graph Data](actions/get-yearly-graph-data.md) | GET | Retrieves yearly issuer graph data from Certs 365. |

### Issuer

| Action | Method | Description |
| --- | --- | --- |
| [Add Trusted Owner](actions/add-trusted-owner.md) | PUT | Adds a trusted owner role in Certs 365. |
| [Create And Validate Issuer](actions/create-and-validate-issuer.md) | POST | Creates and validates an issuer in Certs 365. |
| [Get Issuer By Email](actions/get-issuer-by-email.md) | GET | Retrieves issuer details from Certs 365 by email. |
| [List Issuers](actions/list-issuers.md) | GET | Retrieves issuer details from Certs 365. |
| [Remove Trusted Owner](actions/remove-trusted-owner.md) | PUT | Removes a trusted owner role in Certs 365. |
| [Validate Issuer](actions/validate-issuer.md) | PUT | Validates an issuer in Certs 365. |

### Issuerlog

| Action | Method | Description |
| --- | --- | --- |
| [Get Issuer Logs](actions/get-issuer-logs.md) | GET | Retrieves issuer issue logs from Certs 365. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Details](actions/get-organization-details.md) | GET | Retrieves organization details from Certs 365. |

### Verification

| Action | Method | Description |
| --- | --- | --- |
| [Get Verification Details](actions/get-verification-details.md) | GET | Retrieves course-wise verification details from Certs 365. |

