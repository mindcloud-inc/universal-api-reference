# <img src="https://images.mindcloud.co/apps/icons/cloudmersive-icon_1777991382978.png" alt="Cloudmersive Data Validation logo" width="28" height="28"> Cloudmersive Data Validation: Universal API

Validate emails, domains, URLs, IP addresses, addresses, phone numbers, VAT numbers, names, and text inputs using the Cloudmersive Data Validation API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloudmersiveDataValidation/latest
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloudmersive.com/validate-api
- **Vendor API docs:** https://api.cloudmersive.com/docs/validate.asp

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get IP Intelligence](actions/get-ip-intelligence.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveDataValidation/latest/actions/get-ip-intelligence?connectionId=$CONNECTION_ID&value=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Address Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Street Address](actions/validate-street-address.md) | GET | Validates a street address with Cloudmersive Data Validation. |

### Country Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Country](actions/validate-country.md) | GET | Validates country information with Cloudmersive Data Validation. |

### Domain Quality

| Action | Method | Description |
| --- | --- | --- |
| [Score Domain Quality](actions/score-domain-quality.md) | GET | Scores domain quality with Cloudmersive Data Validation. |

### Domain Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Domain Name](actions/validate-domain-name.md) | GET | Validates a domain name with Cloudmersive Data Validation. |

### Email Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check Email Servers](actions/check-email-servers.md) | GET | Checks email servers for an address with Cloudmersive Data Validation. |
| [Fully Validate Email Address](actions/fully-validate-email-address.md) | GET | Fully validates an email address with Cloudmersive Data Validation. |
| [Validate Email Address Syntax Only](actions/validate-email-address-syntax-only.md) | GET | Validates email address syntax with Cloudmersive Data Validation. |

### Ip Bot Status

| Action | Method | Description |
| --- | --- | --- |
| [Check IP Bot Status](actions/check-ip-bot-status.md) | GET | Checks whether an IP is a bot client. |

### Ip Geolocation

| Action | Method | Description |
| --- | --- | --- |
| [Geolocate IP Address](actions/geolocate-ip-address.md) | GET | Geolocates an IP address with Cloudmersive Data Validation. |

### Ip Intelligence

| Action | Method | Description |
| --- | --- | --- |
| [Get IP Intelligence](actions/get-ip-intelligence.md) | GET | Retrieves IP intelligence from Cloudmersive Data Validation. |

### Ip Threat

| Action | Method | Description |
| --- | --- | --- |
| [Check IP Threat](actions/check-ip-threat.md) | GET | Checks an IP address for threats with Cloudmersive Data Validation. |

### Name Parse

| Action | Method | Description |
| --- | --- | --- |
| [Parse Full Name](actions/parse-full-name.md) | GET | Parses a full name with Cloudmersive Data Validation. |

### Phone Number Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Phone Number](actions/validate-phone-number.md) | GET | Validates a phone number with Cloudmersive Data Validation. |

### Postal Code Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate Postal Code](actions/validate-postal-code.md) | GET | Validates a postal code with Cloudmersive Data Validation. |

### Text Input Validation

| Action | Method | Description |
| --- | --- | --- |
| [Check SQL Injection](actions/check-sql-injection.md) | GET | Checks text input for SQL injection with Cloudmersive Data Validation. |
| [Check XSS](actions/check-xss.md) | GET | Checks text input for XSS with Cloudmersive Data Validation. |

### Tor Exit Node Check

| Action | Method | Description |
| --- | --- | --- |
| [Check Tor Exit Node](actions/check-tor-exit-node.md) | GET | Checks whether an IP is a Tor node. |

### Url Threat Check

| Action | Method | Description |
| --- | --- | --- |
| [Check URL Phishing Threat](actions/check-url-phishing-threat.md) | GET | Checks a URL for phishing threats with Cloudmersive Data Validation. |
| [Check URL Safety Threat](actions/check-url-safety-threat.md) | GET | Checks a URL for safety threats with Cloudmersive Data Validation. |
| [Check URL SSRF Threat](actions/check-url-ssrf-threat.md) | GET | Checks a URL for SSRF threats with Cloudmersive Data Validation. |

### Url Validation

| Action | Method | Description |
| --- | --- | --- |
| [Fully Validate URL](actions/fully-validate-url.md) | GET | Fully validates a URL with Cloudmersive Data Validation. |
| [Validate URL Syntax](actions/validate-url-syntax.md) | GET | Validates URL syntax with Cloudmersive Data Validation. |

### Vat Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate VAT Number](actions/validate-vat-number.md) | GET | Validates a VAT number with Cloudmersive Data Validation. |

