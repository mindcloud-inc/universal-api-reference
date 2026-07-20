# Prembly: Native API Reference

A consolidated summary of Prembly's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://docs.prembly.com/reference
- **API base URL:** `https://api.prembly.com`

## Authentication

### API Key

Server-side API key authentication for Prembly.

### Credentials

- **API Key:** `apiKey` · required
- **Application ID:** `appId` · required · Prembly application identifier required alongside the API key for live authenticated requests.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.prembly.com/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Account with Name Comparism](actions/account-with-name-comparism.md) | `POST /verification/bank_account/comparism` | [docs](https://docs.prembly.com/reference/account-with-name-comparism) |
| [Address Verification](actions/address-verification.md) | `POST /verification/address` | [docs](https://docs.prembly.com/reference/address-verification-1) |
| [Advance Phone Number](actions/advance-phone-number.md) | `POST /verification/phone_number/advance` | [docs](https://docs.prembly.com/reference/advance-phone-number-1) |
| [Bank Account (Basic)](actions/bank-account-basic.md) | `POST /verification/bank_account/basic` | [docs](https://docs.prembly.com/reference/account-number-10-1) |
| [Basic Phone Number](actions/basic-phone-number.md) | `POST /verification/phone_number` | [docs](https://docs.prembly.com/reference/basic-phone-number-1) |
| [Company Search By Person](actions/company-search-by-person.md) | `POST /verification/global/company/search_with_string` | [docs](https://docs.prembly.com/reference/company-search-by-person) |
| [Company Search With Registration Number](actions/company-search-with-registration-number.md) | `POST /verification/global/company` | [docs](https://docs.prembly.com/reference/company-search-with-registration-number-1) |
| [Create Candidate Request](actions/create-candidate-request.md) | `POST /api/v1/api/bgc/requests/candidates/` | [docs](https://docs.prembly.com/reference/create-candidate-request) |
| [Create Custom Package](actions/create-custom-package.md) | `POST /api/v1/api/bgc/packages/` | [docs](https://docs.prembly.com/reference/create-custom-package) |
| [Delete Custom Package](actions/delete-custom-package.md) | `DELETE /api/v1/api/bgc/packages/:packageId/` | [docs](https://docs.prembly.com/reference/delete-custom-package) |
| [Document Verification](actions/document-verification.md) | `POST /verification/document` | [docs](https://docs.prembly.com/reference/document-verification-47) |
| [Document Verification with Face](actions/document-verification-with-face.md) | `POST /verification/document_w_face` | [docs](https://docs.prembly.com/reference/document-verification-with-face) |
| [Face Comparison](actions/face-comparison.md) | `POST /verification/biometrics/face/comparison` | [docs](https://docs.prembly.com/reference/face-comparison) |
| [Face Liveliness Check](actions/face-liveliness-check.md) | `POST /verification/biometrics/face/liveliness_check` | [docs](https://docs.prembly.com/reference/face-liveliness-check) |
| [Face Scan](actions/face-scan.md) | `POST /api/v1/fraud/face-scan/` | [docs](https://docs.prembly.com/reference/face-scan) |
| [Geo-location](actions/geo-location.md) | `POST /verification/address/geolocation/verification` | [docs](https://docs.prembly.com/reference/geo-location) |
| [Get Bulk Fraud Scan Details](actions/get-bulk-fraud-scan-details.md) | `GET /api/v1/fraud/bulk-scan/:bulkId/` | [docs](https://docs.prembly.com/reference/check-status) |
| [Get Candidate Request Detail](actions/get-candidate-request-detail.md) | `GET /requests/candidates/:reference/` | [docs](https://docs.prembly.com/reference/get-candidate-request-detail) |
| [Get Custom Package Detail](actions/get-custom-package-detail.md) | `GET /api/v1/api/bgc/packages/:packageId` | [docs](https://docs.prembly.com/reference/get-custom-package-detail) |
| [Get Fraud Report Detail](actions/get-fraud-report-detail.md) | `GET /api/v1/fraud/reports/:reportId/` | [docs](https://docs.prembly.com/reference/check-status) |
| [Get SDK Session](actions/get-sdk-session.md) | `GET /api/v1/checker-widget/sdk/sessions/` | [docs](https://docs.prembly.com/reference/sdk-session-retrieval) |
| [Get System Package Detail](actions/get-system-package-detail.md) | `GET /api/v1/api/bgc/system-packages/:packageId` | [docs](https://docs.prembly.com/reference/list-system-package) |
| [Get Verification Status](actions/get-verification-status.md) | `GET /verification/:id/status` | [docs](https://docs.prembly.com/reference/get-verification-status-1) |
| [Get Wallet Balance](actions/get-wallet-balance.md) | `GET /api/v1/wallet` | [docs](https://docs.prembly.com/reference/get-wallet-balance-1) |
| [ID Scan](actions/id-scan.md) | `POST /api/v1/fraud/id-scan/` | [docs](https://docs.prembly.com/reference/id-scan) |
| [List All Check Types](actions/list-all-check-types.md) | `GET /api/v1/api/bgc/check-types/` | [docs](https://docs.prembly.com/reference/list-all-check-types) |
| [List Bulk Scan](actions/list-bulk-scan.md) | `GET /api/v1/fraud/bulk-scan/` | [docs](https://docs.prembly.com/reference/bulk-scan) |
| [List Candidate Requests](actions/list-candidate-requests.md) | `GET /api/v1/api/bgc/requests/candidates/` | [docs](https://docs.prembly.com/reference/list-candidate-requests) |
| [List Check Types by Country](actions/list-check-types-by-country.md) | `GET /api/v1/api/bgc/country/check-types/` | [docs](https://docs.prembly.com/reference/list-check-types-by-country) |
| [List Countries](actions/list-countries.md) | `GET /api/v1/api/bgc/countries/` | [docs](https://docs.prembly.com/reference/list-countries) |
| [List Custom Packages](actions/list-custom-packages.md) | `GET /api/v1/api/bgc/packages/` | [docs](https://docs.prembly.com/reference/list-custom-packages) |
| [List Fraud Reports](actions/list-fraud-reports.md) | `GET /api/v1/fraud/reports/` | [docs](https://docs.prembly.com/reference/list-fraud-reports) |
| [List System Packages](actions/list-system-packages.md) | `GET /api/v1/api/bgc/system-packages/` | [docs](https://docs.prembly.com/reference/get-system-package-detail) |
| [PEP and Sanction](actions/pep-and-sanction.md) | `POST /api/v1/verification/aml-screening/` | [docs](https://docs.prembly.com/reference/pep-and-sanction) |
| [Reinitiate Candidate Request](actions/reinitiate-candidate-request.md) | `POST /candidates/:reference/reinitiate/` | [docs](https://docs.prembly.com/reference/reinitiate-candidate-request) |
| [Submit Fraud Report](actions/submit-fraud-report.md) | `POST /api/v1/fraud/reports/submit/` | [docs](https://docs.prembly.com/reference/submit-fraud-report) |
| [Tax Identification Number Check](actions/tax-identification-number-check.md) | `POST /verification/global/tin-check` | [docs](https://docs.prembly.com/reference/tax-identification-number) |
| [Transaction Monitoring Screen Transaction](actions/transaction-monitoring-screen-transaction.md) | `POST /api/v1/fraud/transaction-monitoring/screen-transaction` | [docs](https://docs.prembly.com/reference/tm-transaction-monitoring) |
| [Update Custom Package](actions/update-custom-package.md) | `PUT /api/v1/api/bgc/packages/:packageId/` | [docs](https://docs.prembly.com/reference/update-custom-package) |
| [VIN/CAR CHASIS](actions/vincar-chasis.md) | `POST /verification/vehicle/vin` | [docs](https://docs.prembly.com/reference/vincar-chasis) |
