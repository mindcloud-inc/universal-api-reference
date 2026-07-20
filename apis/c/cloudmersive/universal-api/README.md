# <img src="https://images.mindcloud.co/apps/icons/icon-1_1781294144232.png" alt="Cloudmersive logo" width="28" height="28"> Cloudmersive: Universal API

Cloudmersive provides validation, currency, barcode, OCR, virus scanning, conversion, and other utility APIs through a shared HTTPS endpoint and API key authentication.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloudmersive/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloudmersive.com
- **Vendor API docs:** https://api.cloudmersive.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Date and Time](actions/get-current-date-and-time.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-current-date-and-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Check Country EU Membership](actions/check-country-eu-membership.md) | GET | Checks EU membership for a country in Cloudmersive. |
| [Geocode Address](actions/geocode-address.md) | GET | Geocodes an address in Cloudmersive. |
| [Get Country Currency](actions/get-country-currency.md) | GET | Retrieves a country's currency from Cloudmersive. |
| [Get Country Region](actions/get-country-region.md) | GET | Retrieves a country's region from Cloudmersive. |
| [Get Country Timezones](actions/get-country-timezones.md) | GET | Retrieves country time zones from Cloudmersive. |
| [List ISO 3166-1 Countries](actions/list-iso31661-countries.md) | GET | Retrieves ISO 3166-1 countries from Cloudmersive. |
| [Normalize Street Address](actions/normalize-street-address.md) | GET | Normalizes a street address in Cloudmersive. |
| [Parse Address String](actions/parse-address-string.md) | GET | Parses an address string in Cloudmersive. |
| [Reverse Geocode Address](actions/reverse-geocode-address.md) | GET | Reverse geocodes coordinates into an address in Cloudmersive. |
| [Validate City and State or Province](actions/validate-city-and-state-or-province.md) | GET | Validates a city and state or province in Cloudmersive. |
| [Validate Country](actions/validate-country.md) | GET | Validates country information in Cloudmersive. |
| [Validate Postal Code](actions/validate-postal-code.md) | GET | Validates a postal code in Cloudmersive. |
| [Validate State or Province](actions/validate-state-or-province.md) | GET | Validates a state or province in Cloudmersive. |
| [Validate Street Address](actions/validate-street-address.md) | GET | Validates a street address in Cloudmersive. |

### Currencyexchange

| Action | Method | Description |
| --- | --- | --- |
| [List Available Currencies](actions/list-available-currencies.md) | GET | Retrieves available currencies and countries from Cloudmersive. |

### Datetime

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Date and Time](actions/get-current-date-and-time.md) | GET | Retrieves the current date and time from Cloudmersive. |
| [Get Public Holidays](actions/get-public-holidays.md) | GET | Retrieves public holidays by country and year in Cloudmersive. |
| [Parse Natural Language Date and Time](actions/parse-natural-language-date-and-time.md) | GET | Parses a natural language date and time in Cloudmersive. |
| [Parse Structured Date and Time](actions/parse-structured-date-and-time.md) | GET | Parses a structured date and time in Cloudmersive. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Check URL for Phishing Threats](actions/check-url-for-phishing-threats.md) | GET | Checks a URL for phishing threats in Cloudmersive. |
| [Get Domain Quality Score](actions/get-domain-quality-score.md) | GET | Retrieves a domain quality score from Cloudmersive. |
| [Get Domain WHOIS](actions/get-domain-whois.md) | GET | Retrieves WHOIS data for a domain in Cloudmersive. |
| [Get Top-Level Domain From URL](actions/get-top-level-domain-from-url.md) | GET | Retrieves a top-level domain from a URL in Cloudmersive. |
| [Validate Domain](actions/validate-domain.md) | GET | Validates a domain in Cloudmersive. |
| [Validate URL Fully](actions/validate-url-fully.md) | GET | Validates a URL fully in Cloudmersive. |
| [Validate URL Syntax](actions/validate-url-syntax.md) | GET | Validates a URL syntactically in Cloudmersive. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Validate Email Fully](actions/validate-email-fully.md) | GET | Fully validates an email address in Cloudmersive. |
| [Validate Email Partially](actions/validate-email-partially.md) | GET | Partially validates an email address in Cloudmersive. |
| [Validate Email Syntax](actions/validate-email-syntax.md) | GET | Validates an email address syntactically in Cloudmersive. |

### Ipaddress

| Action | Method | Description |
| --- | --- | --- |
| [Get IP Intelligence](actions/get-ip-intelligence.md) | GET | Retrieves IP intelligence from Cloudmersive. |

