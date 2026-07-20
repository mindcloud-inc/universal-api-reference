# FCA: Native API Reference

A consolidated summary of FCA's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://register.fca.org.uk/Developer/s/
- **API base URL:** `https://register.fca.org.uk/services/V0.1`

## Authentication

### FCA API key

Authenticate with the email address used for the FCA Developer portal and the API key from the registration profile.

### Credentials

- **API key:** `apiKey` · required
- **API email:** `apiEmail` · required · Email address used to register for FCA Developer portal access.

Send these headers with each API request:

```http
X-AUTH-KEY: <apiKey>
X-AUTH-EMAIL: <apiEmail>
```

[Official authentication documentation](https://register.fca.org.uk/Developer/s/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `Data`.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get firm](actions/get-firm.md) | `GET /Firm/:frn` | [docs](https://register.fca.org.uk/Developer/s/) |
| [Get fund](actions/get-fund.md) | `GET /CIS/:prn` | [docs](https://register.fca.org.uk/Developer/s/) |
| [Get individual](actions/get-individual.md) | `GET /Individuals/:irn` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List firm addresses](actions/list-firm-addresses.md) | `GET /Firm/:frn/Address` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List firm appointed representatives](actions/list-firm-appointed-representatives.md) | `GET /Firm/:frn/AR` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List firm controlled functions](actions/list-firm-controlled-functions.md) | `GET /Firm/:frn/CF` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List firm disciplinary history](actions/list-firm-disciplinary-history.md) | `GET /Firm/:frn/DisciplinaryHistory` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List firm exclusions](actions/list-firm-exclusions.md) | `GET /Firm/:frn/Exclusions` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List firm individuals](actions/list-firm-individuals.md) | `GET /Firm/:frn/Individuals` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List firm names](actions/list-firm-names.md) | `GET /Firm/:frn/Names` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List firm passport permissions](actions/list-firm-passport-permissions.md) | `GET /Firm/:frn/Passports/:country/Permission` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List firm passports](actions/list-firm-passports.md) | `GET /Firm/:frn/Passports` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List firm permissions](actions/list-firm-permissions.md) | `GET /Firm/:frn/Permissions` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List firm regulators](actions/list-firm-regulators.md) | `GET /Firm/:frn/Regulators` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List firm requirement investment types](actions/list-firm-requirement-investment-types.md) | `GET /Firm/:frn/Requirements/:reqRef/InvestmentTypes` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List firm requirements](actions/list-firm-requirements.md) | `GET /Firm/:frn/Requirements` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List firm waivers](actions/list-firm-waivers.md) | `GET /Firm/:frn/Waivers` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List fund names](actions/list-fund-names.md) | `GET /CIS/:prn/Names` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List fund subfunds](actions/list-fund-subfunds.md) | `GET /CIS/:prn/Subfund` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List individual controlled functions](actions/list-individual-controlled-functions.md) | `GET /Individuals/:irn/CF` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List individual disciplinary history](actions/list-individual-disciplinary-history.md) | `GET /Individuals/:irn/DisciplinaryHistory` | [docs](https://register.fca.org.uk/Developer/s/) |
| [List regulated markets](actions/list-regulated-markets.md) | `GET /CommonSearch` | [docs](https://register.fca.org.uk/Developer/s/) |
| [Search firms](actions/search-firms.md) | `GET /Search` | [docs](https://register.fca.org.uk/Developer/s/) |
| [Search funds](actions/search-funds.md) | `GET /Search` | [docs](https://register.fca.org.uk/Developer/s/) |
| [Search individuals](actions/search-individuals.md) | `GET /Search` | [docs](https://register.fca.org.uk/Developer/s/) |
