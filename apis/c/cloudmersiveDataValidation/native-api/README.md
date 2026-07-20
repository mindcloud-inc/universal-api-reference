# Cloudmersive Data Validation: Native API Reference

A consolidated summary of Cloudmersive Data Validation's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://api.cloudmersive.com/docs/validate.asp
- **OpenAPI specification:** https://api-console.cloudmersive.com/swagger/api/validate
- **API base URL:** `https://api.cloudmersive.com`

## Authentication

### Cloudmersive API Key

Cloudmersive Data Validation uses API key authentication in the Apikey request header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Apikey: <apiKey>
```

[Official authentication documentation](https://api.cloudmersive.com/docs/validate.asp)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Email Servers](actions/check-email-servers.md) | `POST /validate/email/address/servers` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Check IP Bot Status](actions/check-ip-bot-status.md) | `POST /validate/ip/is-bot` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Check IP Threat](actions/check-ip-threat.md) | `POST /validate/ip/is-threat` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Check SQL Injection](actions/check-sql-injection.md) | `POST /validate/text-input/check/sql-injection` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Check Tor Exit Node](actions/check-tor-exit-node.md) | `POST /validate/ip/is-tor-node` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Check URL Phishing Threat](actions/check-url-phishing-threat.md) | `POST /validate/domain/url/phishing-threat-check` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Check URL Safety Threat](actions/check-url-safety-threat.md) | `POST /validate/domain/url/safety-threat-check` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Check URL SSRF Threat](actions/check-url-ssrf-threat.md) | `POST /validate/domain/url/ssrf-threat-check` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Check XSS](actions/check-xss.md) | `POST /validate/text-input/check/xss` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Fully Validate Email Address](actions/fully-validate-email-address.md) | `POST /validate/email/address/full` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Fully Validate URL](actions/fully-validate-url.md) | `POST /validate/domain/url/full` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Geolocate IP Address](actions/geolocate-ip-address.md) | `POST /validate/ip/geolocate` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Get IP Intelligence](actions/get-ip-intelligence.md) | `POST /validate/ip/intelligence` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Parse Full Name](actions/parse-full-name.md) | `POST /validate/name/full-name` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Score Domain Quality](actions/score-domain-quality.md) | `POST /validate/domain/quality-score` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Validate Country](actions/validate-country.md) | `POST /validate/address/country` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Validate Domain Name](actions/validate-domain-name.md) | `POST /validate/domain/check` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Validate Email Address Syntax Only](actions/validate-email-address-syntax-only.md) | `POST /validate/email/address/syntaxOnly` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Validate Phone Number](actions/validate-phone-number.md) | `POST /validate/phonenumber/basic` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Validate Postal Code](actions/validate-postal-code.md) | `POST /validate/address/postal-code` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Validate Street Address](actions/validate-street-address.md) | `POST /validate/address/street-address` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Validate URL Syntax](actions/validate-url-syntax.md) | `POST /validate/domain/url/syntax-only` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
| [Validate VAT Number](actions/validate-vat-number.md) | `POST /validate/vat/lookup` | [docs](https://api.cloudmersive.com/docs/validate.asp) |
