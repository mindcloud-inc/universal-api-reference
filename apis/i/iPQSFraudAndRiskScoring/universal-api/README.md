# IPQS Fraud and Risk Scoring: Universal API

IPQS Fraud and Risk Scoring provides API-based fraud prevention, risk scoring, and validation tools for IP addresses, email addresses, phone numbers, URLs, devices, and related account intelligence.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/iPQSFraudAndRiskScoring/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.ipqualityscore.com/
- **Vendor API docs:** https://www.ipqualityscore.com/documentation/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Countries](actions/list-countries.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/iPQSFraudAndRiskScoring/latest/actions/list-countries?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Account Credit Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Credit Usage](actions/get-account-credit-usage.md) | GET | Retrieves account credit usage details from IPQS. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [List Countries](actions/list-countries.md) | GET | Retrieves country codes and names from IPQS. |

### Device Fingerprint Postback

| Action | Method | Description |
| --- | --- | --- |
| [Update Device Fingerprint Postback](actions/update-device-fingerprint-postback.md) | PUT | Updates device fingerprint postback data in IPQS. |

### Device Fingerprint Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Device Fingerprint Result](actions/get-device-fingerprint-result.md) | GET | Retrieves device fingerprint verification results from IPQS. |

### Device Tracker Request

| Action | Method | Description |
| --- | --- | --- |
| [List Device Tracker Requests](actions/list-device-tracker-requests.md) | GET | Retrieves previous device fingerprint requests from IPQS. |

### Email Request

| Action | Method | Description |
| --- | --- | --- |
| [List Email Requests](actions/list-email-requests.md) | GET | Retrieves previous email validation requests from IPQS. |

### Email Request Postback

| Action | Method | Description |
| --- | --- | --- |
| [Update Email Request Postback](actions/update-email-request-postback.md) | PUT | Updates email validation request postback data in IPQS. |

### Email Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Email](actions/validate-email.md) | GET | Retrieves email validation and fraud data from IPQS. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get CSV Status And Download Links](actions/get-csv-status-and-download-links.md) | GET | Retrieves CSV processing status and download links from IPQS. |
| [List CSV Uploads](actions/list-csv-uploads.md) | GET | Retrieves uploaded CSV jobs from IPQS. |
| [Lookup Malware Scan](actions/lookup-malware-scan.md) | GET | Retrieves malware scan results from IPQS. |
| [Scan Malware File](actions/scan-malware-file.md) | POST | Creates a malware scan for a file with IPQS. |
| [Scan Malware URL](actions/scan-malware-url.md) | POST | Creates a malware scan for a URL with IPQS. |
| [Upload Bulk Email CSV](actions/upload-bulk-email-csv.md) | POST | Uploads a bulk email validation CSV to IPQS. |
| [Upload Bulk IP CSV](actions/upload-bulk-ip-csv.md) | POST | Uploads a bulk IP validation CSV to IPQS. |
| [Upload Bulk Phone CSV](actions/upload-bulk-phone-csv.md) | POST | Uploads a bulk phone validation CSV to IPQS. |
| [Upload Bulk URL CSV](actions/upload-bulk-url-csv.md) | POST | Uploads a bulk URL scan CSV to IPQS. |

### Fraud Report

| Action | Method | Description |
| --- | --- | --- |
| [Report Fraudulent Email](actions/report-fraudulent-email.md) | POST | Reports a fraudulent email address to IPQS. |
| [Report Fraudulent IP](actions/report-fraudulent-ip.md) | POST | Reports a fraudulent IP address to IPQS. |
| [Report Fraudulent Phone](actions/report-fraudulent-phone.md) | POST | Reports a fraudulent phone number to IPQS. |
| [Report Fraudulent Request](actions/report-fraudulent-request.md) | POST | Reports a fraudulent event to IPQS. |

### Ip Risk Score

| Action | Method | Description |
| --- | --- | --- |
| [Score IP Address](actions/score-ip-address.md) | GET | Retrieves IP fraud and proxy risk details from IPQS. |

### Leaked Credential Search

| Action | Method | Description |
| --- | --- | --- |
| [Search Leaked Email And Password](actions/search-leaked-email-and-password.md) | GET | Retrieves dark web leak matches for an email-password pair from IPQS. |

### Leaked Email Search

| Action | Method | Description |
| --- | --- | --- |
| [Search Leaked Email](actions/search-leaked-email.md) | GET | Retrieves dark web leak matches for an email from IPQS. |

### Leaked Password Search

| Action | Method | Description |
| --- | --- | --- |
| [Search Leaked Password](actions/search-leaked-password.md) | GET | Retrieves dark web leak matches for a password from IPQS. |

### Leaked Username Search

| Action | Method | Description |
| --- | --- | --- |
| [Search Leaked Username](actions/search-leaked-username.md) | GET | Retrieves dark web leak matches for a username from IPQS. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create Allowlist Entry](actions/create-allowlist-entry.md) | POST | Creates a new allowlist entry in IPQS. |
| [Create Blocklist Entry](actions/create-blocklist-entry.md) | POST | Creates a new blocklist entry in IPQS. |
| [Delete Allowlist Entry](actions/delete-allowlist-entry.md) | DELETE | Deletes an existing allowlist entry from IPQS. |
| [Delete Blocklist Entry](actions/delete-blocklist-entry.md) | DELETE | Deletes an existing blocklist entry from IPQS. |
| [List Allowlist Entries](actions/list-allowlist-entries.md) | GET | Retrieves current allowlist entries from IPQS. |
| [List Blocklist Entries](actions/list-blocklist-entries.md) | GET | Retrieves current blocklist entries from IPQS. |

### Login History

| Action | Method | Description |
| --- | --- | --- |
| [Get Login History](actions/get-login-history.md) | GET | Retrieves account login history from IPQS. |

### Mobile Tracker Request

| Action | Method | Description |
| --- | --- | --- |
| [List Mobile Tracker Requests](actions/list-mobile-tracker-requests.md) | GET | Retrieves previous mobile tracker requests from IPQS. |

### Phone Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Phone Number](actions/validate-phone-number.md) | GET | Retrieves phone validation and carrier details from IPQS. |

### Proxy Request

| Action | Method | Description |
| --- | --- | --- |
| [List Proxy Requests](actions/list-proxy-requests.md) | GET | Retrieves previous proxy detection requests from IPQS. |

### Proxy Request Postback

| Action | Method | Description |
| --- | --- | --- |
| [Update Proxy Request Postback](actions/update-proxy-request-postback.md) | PUT | Updates proxy detection request postback data in IPQS. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Device Fingerprint Stats](actions/get-device-fingerprint-stats.md) | GET | Retrieves device fingerprint statistics from IPQS. |

### Transaction Risk Score

| Action | Method | Description |
| --- | --- | --- |
| [Score IP Transaction](actions/score-ip-transaction.md) | GET | Retrieves transaction risk scoring for an IP from IPQS. |

### Url Risk Scan

| Action | Method | Description |
| --- | --- | --- |
| [Scan URL Or Domain](actions/scan-url-or-domain.md) | GET | Retrieves malicious URL scan results from IPQS. |

