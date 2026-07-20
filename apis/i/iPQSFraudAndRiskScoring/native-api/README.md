# IPQS Fraud and Risk Scoring: Native API Reference

A consolidated summary of IPQS Fraud and Risk Scoring's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://www.ipqualityscore.com/documentation/overview
- **API base URL:** `https://www.ipqualityscore.com/api/json`

## Authentication

### API Key

Authenticate IPQS API requests with an IPQS API key created and managed in the IPQS dashboard.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
ipqs-key: <apiKey>
```

[Official authentication documentation](https://www.ipqualityscore.com/documentation/about-ipqs-apis/submitting-data-to-ipqs-apis)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `countries`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Allowlist Entry](actions/create-allowlist-entry.md) | `POST /allowlist/create/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/allowlist-api/allowlist-creating-entries) |
| [Create Blocklist Entry](actions/create-blocklist-entry.md) | `POST /blocklist/create/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/allowlist-api/blocklist-creating-entries) |
| [Delete Allowlist Entry](actions/delete-allowlist-entry.md) | `POST /allowlist/delete/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/allowlist-api/allowlist-deleting-entries) |
| [Delete Blocklist Entry](actions/delete-blocklist-entry.md) | `POST /blocklist/delete/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/allowlist-api/blocklist-deleting-entries) |
| [Get Account Credit Usage](actions/get-account-credit-usage.md) | `GET /account/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/account-management/usage) |
| [Get CSV Status And Download Links](actions/get-csv-status-and-download-links.md) | `GET /csv/{{credentials.apiKey}}/status/:csvId` | [docs](https://www.ipqualityscore.com/documentation/csv-api/check-csv-status) |
| [Get Device Fingerprint Result](actions/get-device-fingerprint-result.md) | `GET https://www.ipqualityscore.com/api/tracker/results/{{credentials.apiKey}}/:ip/:deviceId` | [docs](https://www.ipqualityscore.com/documentation/device-fingerprint-api/verification) |
| [Get Device Fingerprint Stats](actions/get-device-fingerprint-stats.md) | `POST /webhooks/ExampleIntegration/json/device_tracker_statistics` | [docs](https://www.ipqualityscore.com/documentation/integrations/device-tracker-statistics) |
| [Get Login History](actions/get-login-history.md) | `GET /loginhistory/{{credentials.apiKey}}/` | [docs](https://www.ipqualityscore.com/documentation/account-management/login-history) |
| [List Allowlist Entries](actions/list-allowlist-entries.md) | `GET /allowlist/list/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/allowlist-api/allowlist-listing-entries) |
| [List Blocklist Entries](actions/list-blocklist-entries.md) | `GET /blocklist/list/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/allowlist-api/blocklist-listing-entries) |
| [List Countries](actions/list-countries.md) | `GET /country/list` | [docs](https://www.ipqualityscore.com/documentation/countries/overview) |
| [List CSV Uploads](actions/list-csv-uploads.md) | `GET /csv/list` | [docs](https://www.ipqualityscore.com/documentation/csv-api/retrieve-csv-list) |
| [List Device Tracker Requests](actions/list-device-tracker-requests.md) | `GET /requests/{{credentials.apiKey}}/list` | [docs](https://www.ipqualityscore.com/documentation/request-list/overview) |
| [List Email Requests](actions/list-email-requests.md) | `GET /requests/{{credentials.apiKey}}/list` | [docs](https://www.ipqualityscore.com/documentation/request-list/overview) |
| [List Mobile Tracker Requests](actions/list-mobile-tracker-requests.md) | `GET /requests/{{credentials.apiKey}}/list` | [docs](https://www.ipqualityscore.com/documentation/request-list/overview) |
| [List Proxy Requests](actions/list-proxy-requests.md) | `GET /requests/{{credentials.apiKey}}/list` | [docs](https://www.ipqualityscore.com/documentation/request-list/overview) |
| [Lookup Malware Scan](actions/lookup-malware-scan.md) | `POST /malware/lookup/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/malware-file-scanner-api/overview) |
| [Report Fraudulent Email](actions/report-fraudulent-email.md) | `GET /report/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/fraud-reporting/overview) |
| [Report Fraudulent IP](actions/report-fraudulent-ip.md) | `GET /report/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/fraud-reporting/overview) |
| [Report Fraudulent Phone](actions/report-fraudulent-phone.md) | `GET /report/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/fraud-reporting/overview) |
| [Report Fraudulent Request](actions/report-fraudulent-request.md) | `GET /report/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/fraud-reporting/overview) |
| [Scan Malware File](actions/scan-malware-file.md) | `POST /malware/scan/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/malware-file-scanner-api/overview) |
| [Scan Malware URL](actions/scan-malware-url.md) | `POST /malware/scan/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/malware-file-scanner-api/overview) |
| [Scan URL Or Domain](actions/scan-url-or-domain.md) | `GET /url/{{credentials.apiKey}}/:url` | [docs](https://www.ipqualityscore.com/documentation/malicious-url-scanner-api/overview) |
| [Score IP Address](actions/score-ip-address.md) | `GET /ip/{{credentials.apiKey}}/:ip` | [docs](https://www.ipqualityscore.com/documentation/proxy-detection-api/overview) |
| [Score IP Transaction](actions/score-ip-transaction.md) | `GET /ip/{{credentials.apiKey}}/:ip` | [docs](https://www.ipqualityscore.com/documentation/proxy-detection-api/transaction-scoring) |
| [Search Leaked Email](actions/search-leaked-email.md) | `GET /leaked/email/{{credentials.apiKey}}/:email` | [docs](https://www.ipqualityscore.com/documentation/dark-web-leak-api/overview) |
| [Search Leaked Email And Password](actions/search-leaked-email-and-password.md) | `POST /leaked/emailpass/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/dark-web-leak-api/overview) |
| [Search Leaked Password](actions/search-leaked-password.md) | `POST /leaked/password/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/dark-web-leak-api/overview) |
| [Search Leaked Username](actions/search-leaked-username.md) | `GET /leaked/username/{{credentials.apiKey}}/:username` | [docs](https://www.ipqualityscore.com/documentation/dark-web-leak-api/overview) |
| [Update Device Fingerprint Postback](actions/update-device-fingerprint-postback.md) | `GET /postback/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/device-fingerprint-api/conversions) |
| [Update Email Request Postback](actions/update-email-request-postback.md) | `GET /postback/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/email-validation-api/conversions) |
| [Update Proxy Request Postback](actions/update-proxy-request-postback.md) | `GET /postback/{{credentials.apiKey}}` | [docs](https://www.ipqualityscore.com/documentation/proxy-detection-api/conversions) |
| [Upload Bulk Email CSV](actions/upload-bulk-email-csv.md) | `POST /csv/upload` | [docs](https://www.ipqualityscore.com/documentation/csv-api/uploading-csvs) |
| [Upload Bulk IP CSV](actions/upload-bulk-ip-csv.md) | `POST /csv/upload` | [docs](https://www.ipqualityscore.com/documentation/csv-api/uploading-csvs) |
| [Upload Bulk Phone CSV](actions/upload-bulk-phone-csv.md) | `POST /csv/upload` | [docs](https://www.ipqualityscore.com/documentation/csv-api/uploading-csvs) |
| [Upload Bulk URL CSV](actions/upload-bulk-url-csv.md) | `POST /csv/upload` | [docs](https://www.ipqualityscore.com/documentation/csv-api/uploading-csvs) |
| [Validate Email](actions/validate-email.md) | `GET /email/{{credentials.apiKey}}/:email` | [docs](https://www.ipqualityscore.com/documentation/email-validation-api/overview) |
| [Validate Phone Number](actions/validate-phone-number.md) | `GET /phone/{{credentials.apiKey}}/:phone` | [docs](https://www.ipqualityscore.com/documentation/phone-number-validation-api/overview) |
