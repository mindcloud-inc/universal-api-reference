# Certs 365: Native API Reference

A consolidated summary of Certs 365's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://help.certs365.io/documentation/api-endpoints/
- **API base URL:** `https://api1.certs365.io`

## Authentication

### API Key

Bearer JWT token used for authenticated Certs 365 API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.certs365.io/documentation/api-endpoints/authentication/)

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Trusted Owner](actions/add-trusted-owner.md) | `POST /api/add-trusted-owner` | [docs](https://help.certs365.io/documentation/blockchain/add-trusted-owner-grant-role/) |
| [Check Balance](actions/check-balance.md) | `GET /api/check-balance` | [docs](https://help.certs365.io/documentation/blockchain/check-balance-matic/) |
| [Create And Validate Issuer](actions/create-and-validate-issuer.md) | `POST /api/create-validate-issuer` | [docs](https://help.certs365.io/documentation/blockchain/create-validate-issuer-internal/) |
| [Find Certificate](actions/find-certificate.md) | `POST /api/get-issue` | [docs](https://help.certs365.io/documentation/fetching-upload-request-details/get-a-specific-certificate-on-id-or-name-based-search/) |
| [Get Batch Certificates](actions/get-batch-certificates.md) | `POST /api/get-batch-certificates` | [docs](https://help.certs365.io/documentation/fetching-upload-request-details/get-batch-certifications-from-s3/) |
| [Get Issuer By Email](actions/get-issuer-by-email.md) | `POST /api/get-issuer-by-email` | [docs](https://help.certs365.io/documentation/fetching-upload-request-details/get-issuer-details-by-email/) |
| [Get Issuer Logs](actions/get-issuer-logs.md) | `POST /api/get-issuers-log` | [docs](https://help.certs365.io/documentation/fetching-upload-request-details/get-issues-under-criterion-for-admin-dashboard/) |
| [Get Organization Details](actions/get-organization-details.md) | `GET /api/get-organization-details` | [docs](https://help.certs365.io/documentation/fetching-upload-request-details/get-organizations-details-unique-list-for-mobile-application/) |
| [Get Organization Issues](actions/get-organization-issues.md) | `POST /api/get-organization-issues` | [docs](https://help.certs365.io/documentation/fetching-upload-request-details/get-certification-issued-with-given-name-by-issuer-under-the-organization-mobile-application/) |
| [Get Single Certificates](actions/get-single-certificates.md) | `POST /api/get-single-certificates` | [docs](https://help.certs365.io/documentation/fetching-upload-request-details/get-single-with-without-pdf-certifications-from-s3/) |
| [Get Status Graph Data](actions/get-status-graph-data.md) | `GET /api/get-status-graph-data/{month}/{year}/{email}` | [docs](https://help.certs365.io/documentation/fetching-upload-request-details/get-graph-endpoints-features-of-the-issuer-based-on-month-year/) |
| [Get Verification Details](actions/get-verification-details.md) | `POST /api/get-verification-details` | [docs](https://help.certs365.io/documentation/fetching-upload-request-details/get-verification-details-of-issuer-course-wise/) |
| [Get Yearly Graph Data](actions/get-yearly-graph-data.md) | `GET /api/get-graph-data/{year}/{email}` | [docs](https://help.certs365.io/documentation/fetching-upload-request-details/get-graph-endpoints-of-issuer-based-on-the-input-year/) |
| [Issue Batch Certificates](actions/issue-batch-certificates.md) | `POST /api/batch-certificate-issue` | [docs](https://help.certs365.io/documentation/code-module-apis/issue-batch-certification-excel/) |
| [Issue Certificate](actions/issue-certificate.md) | `POST /api/issue` | [docs](https://help.certs365.io/documentation/code-module-apis/issue-certification-details/) |
| [Issue Certificate PDF](actions/issue-certificate-pdf.md) | `POST /api/issue-pdf` | [docs](https://help.certs365.io/documentation/code-module-apis/issue-certification-pdf/) |
| [List Issuers](actions/list-issuers.md) | `GET /api/get-all-issuers/` | [docs](https://help.certs365.io/documentation/fetching-upload-request-details/get-details-of-issuers-unapproved/) |
| [Remove Trusted Owner](actions/remove-trusted-owner.md) | `POST /api/remove-trusted-owner` | [docs](https://help.certs365.io/documentation/blockchain/remove-trusted-owner-revoke-role/) |
| [Renew Batch](actions/renew-batch.md) | `POST /api/renew-batch` | [docs](https://help.certs365.io/documentation/code-module-apis/renew-certification-extend-expiration-batch/) |
| [Renew Certificate](actions/renew-certificate.md) | `POST /api/renew-cert` | [docs](https://help.certs365.io/documentation/code-module-apis/renew-certification-extend-expiration-single/) |
| [Update Batch Status](actions/update-batch-status.md) | `POST /api/update-batch-status` | [docs](https://help.certs365.io/documentation/code-module-apis/revoke-reactivate-certification-batch/) |
| [Update Certificate Status](actions/update-certificate-status.md) | `POST /api/update-cert-status` | [docs](https://help.certs365.io/documentation/code-module-apis/revoke-reactivate-certification-single/) |
| [Upload Certificate Asset](actions/upload-certificate-asset.md) | `POST /api/upload-certificate` | [docs](https://help.certs365.io/documentation/fetching-upload-request-details/upload-certification-into-aws-s3/) |
| [Upload Media File](actions/upload-media-file.md) | `POST /api/upload` | [docs](https://help.certs365.io/documentation/fetching-upload-request-details/upload-media-file-into-s3/) |
| [Validate Issuer](actions/validate-issuer.md) | `POST /api/validate-issuer` | [docs](https://help.certs365.io/documentation/blockchain/validate-issuer/) |
