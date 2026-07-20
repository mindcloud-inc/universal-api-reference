# Cloudmersive: Native API Reference

A consolidated summary of Cloudmersive's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.cloudmersive.com/
- **API base URL:** `https://api.cloudmersive.com`

## Authentication

### API Key

Cloudmersive API key provided through the Apikey request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Apikey: <apiKey>
```

[Official authentication documentation](https://api.cloudmersive.com/docs/validate.asp)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Country EU Membership](actions/check-country-eu-membership.md) | `POST /validate/address/country/check-eu-membership` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-country-check-eu-membership-post) |
| [Check URL for Phishing Threats](actions/check-url-for-phishing-threats.md) | `POST /validate/domain/url/phishing-threat-check` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-domain-url-phishing-threat-check-post) |
| [Geocode Address](actions/geocode-address.md) | `POST /validate/address/geocode` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-geocode-post) |
| [Get Country Currency](actions/get-country-currency.md) | `POST /validate/address/country/get-currency` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-country-get-currency-post) |
| [Get Country Region](actions/get-country-region.md) | `POST /validate/address/country/get-region` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-country-get-region-post) |
| [Get Country Timezones](actions/get-country-timezones.md) | `POST /validate/address/country/get-timezones` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-country-get-timezones-post) |
| [Get Current Date and Time](actions/get-current-date-and-time.md) | `GET /validate/date-time/get/now` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-date-time-get-now-get) |
| [Get Domain Quality Score](actions/get-domain-quality-score.md) | `POST /validate/domain/quality-score` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-domain-quality-score-post) |
| [Get Domain WHOIS](actions/get-domain-whois.md) | `POST /validate/domain/whois` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-domain-whois-post) |
| [Get IP Intelligence](actions/get-ip-intelligence.md) | `POST /validate/ip/intelligence` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-ip-intelligence-post) |
| [Get Public Holidays](actions/get-public-holidays.md) | `POST /validate/date-time/get/holidays` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-date-time-get-holidays-post) |
| [Get Top-Level Domain From URL](actions/get-top-level-domain-from-url.md) | `POST /validate/domain/url/get-top-level-domain` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-domain-url-get-top-level-domain-post) |
| [List Available Currencies](actions/list-available-currencies.md) | `POST /currency/exchange-rates/list-available` | [docs](https://api.cloudmersive.com/docs/currency.asp#operation--currency-exchange-rates-list-available-post) |
| [List ISO 3166-1 Countries](actions/list-iso31661-countries.md) | `POST /validate/address/country/list` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-country-list-post) |
| [Normalize Street Address](actions/normalize-street-address.md) | `POST /validate/address/street-address/normalize` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-street-address-normalize-post) |
| [Parse Address String](actions/parse-address-string.md) | `POST /validate/address/parse` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-parse-post) |
| [Parse Natural Language Date and Time](actions/parse-natural-language-date-and-time.md) | `POST /validate/date-time/parse/date-time/natural-language` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-date-time-parse-date-time-natural-language-post) |
| [Parse Structured Date and Time](actions/parse-structured-date-and-time.md) | `POST /validate/date-time/parse/date-time/structured` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-date-time-parse-date-time-structured-post) |
| [Reverse Geocode Address](actions/reverse-geocode-address.md) | `POST /validate/address/geocode/reverse` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-geocode-reverse-post) |
| [Validate City and State or Province](actions/validate-city-and-state-or-province.md) | `POST /validate/address/city` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-city-post) |
| [Validate Country](actions/validate-country.md) | `POST /validate/address/country` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-country-post) |
| [Validate Domain](actions/validate-domain.md) | `POST /validate/domain/check` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-domain-check-post) |
| [Validate Email Fully](actions/validate-email-fully.md) | `POST /validate/email/address/full` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-email-address-full-post) |
| [Validate Email Partially](actions/validate-email-partially.md) | `POST /validate/email/address/servers` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-email-address-servers-post) |
| [Validate Email Syntax](actions/validate-email-syntax.md) | `POST /validate/email/address/syntaxOnly` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-email-address-syntaxOnly-post) |
| [Validate Postal Code](actions/validate-postal-code.md) | `POST /validate/address/postal-code` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-postal-code-post) |
| [Validate State or Province](actions/validate-state-or-province.md) | `POST /validate/address/state` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-state-post) |
| [Validate Street Address](actions/validate-street-address.md) | `POST /validate/address/street-address` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-address-street-address-post) |
| [Validate URL Fully](actions/validate-url-fully.md) | `POST /validate/domain/url/full` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-domain-url-full-post) |
| [Validate URL Syntax](actions/validate-url-syntax.md) | `POST /validate/domain/url/syntax-only` | [docs](https://api.cloudmersive.com/docs/validate.asp#operation--validate-domain-url-syntax-only-post) |
