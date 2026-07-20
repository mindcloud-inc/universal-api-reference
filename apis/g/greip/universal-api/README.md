# <img src="https://images.mindcloud.co/apps/icons/images_1775137462966.png" alt="Greip - Fraud Prevention logo" width="28" height="28"> Greip - Fraud Prevention: Universal API

Greip - Fraud Prevention provides IP intelligence, validation, and fraud-scoring APIs for geolocation, reputation checks, email and phone verification, domain and BIN/IBAN lookup, and payment risk analysis.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/greip/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://greip.io
- **Vendor API docs:** https://docs.greip.io/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get IP Geolocation](actions/get-ip-geolocation.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/greip/latest/actions/get-ip-geolocation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Asn

| Action | Method | Description |
| --- | --- | --- |
| [Get ASN Lookup](actions/get-asn-lookup.md) | GET | Retrieves ASN lookup data from Greip. |

### Bin

| Action | Method | Description |
| --- | --- | --- |
| [Get BIN/IIN Lookup](actions/get-bin-iin-lookup.md) | GET | Retrieves BIN/IIN lookup data from Greip. |

### Country

| Action | Method | Description |
| --- | --- | --- |
| [Get Country Lookup](actions/get-country-lookup.md) | GET | Retrieves country lookup data from Greip. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Lookup](actions/get-domain-lookup.md) | GET | Retrieves domain lookup data from Greip. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Scoring](actions/get-email-scoring.md) | GET | Retrieves email risk scoring from Greip. |

### Iban

| Action | Method | Description |
| --- | --- | --- |
| [Get IBAN Lookup](actions/get-iban-lookup.md) | GET | Retrieves IBAN lookup data from Greip. |

### Ip

| Action | Method | Description |
| --- | --- | --- |
| [Get Bulk IP Lookup](actions/get-bulk-ip-lookup.md) | GET | Retrieves lookup data for multiple IP addresses from Greip. |
| [Get Free IP](actions/get-free-ip.md) | GET | Retrieves a visitor's IP address from Greip. |
| [Get IP Geolocation](actions/get-ip-geolocation.md) | GET | Retrieves IP geolocation data from Greip. |
| [Get IP Lookup](actions/get-ip-lookup.md) | GET | Retrieves lookup data for an IP address from Greip. |
| [Get IP Reputation](actions/get-ip-reputation.md) | GET | Retrieves IP reputation data from Greip. |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Run Payment Fraud Detection](actions/run-payment-fraud-detection.md) | GET | Runs payment fraud detection in Greip. |

### Phone Number

| Action | Method | Description |
| --- | --- | --- |
| [Get Phone Number Scoring](actions/get-phone-number-scoring.md) | GET | Retrieves phone number risk scoring from Greip. |

### Text

| Action | Method | Description |
| --- | --- | --- |
| [Get Profanity Detection](actions/get-profanity-detection.md) | GET | Detects profanity in text with Greip. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Delete User Data](actions/delete-user-data.md) | DELETE | Deletes stored user data from Greip. |

