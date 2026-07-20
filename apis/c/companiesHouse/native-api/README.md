# Companies House: Native API Reference

A consolidated summary of Companies House's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference
- **OpenAPI specification:** https://developer-specs.company-information.service.gov.uk/api.ch.gov.uk-specifications/swagger-2.0/spec/swagger.json
- **API base URL:** `https://api.company-information.service.gov.uk`

## Authentication

### Companies House API Key

HTTP Basic authentication using the Companies House REST API key as the username and a blank password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developer.company-information.service.gov.uk/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Company Charge](actions/get-company-charge.md) | `GET /company/:company_number/charges/:charge_id` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/charges/get) |
| [Get Company Exemptions](actions/get-company-exemptions.md) | `GET /company/:company_number/exemptions` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/exemptions/company) |
| [Get Company Filing History Item](actions/get-company-filing-history-item.md) | `GET /company/:company_number/filing-history/:transaction_id` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/filing-history/list) |
| [Get Company Insolvency](actions/get-company-insolvency.md) | `GET /company/:company_number/insolvency` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/insolvency/get) |
| [Get Company Officer Appointment](actions/get-company-officer-appointment.md) | `GET /company/:company_number/appointments/:appointment_id` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/officers/appointment) |
| [Get Company Profile](actions/get-company-profile.md) | `GET /company/:company_number` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/company-profile) |
| [Get Company PSC Corporate Entity](actions/get-company-psc-corporate-entity.md) | `GET /company/:company_number/persons-with-significant-control/corporate-entity/:psc_id` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/persons-with-significant-control/corporate-entity/get) |
| [Get Company PSC Corporate Entity Beneficial Owner](actions/get-company-psc-corporate-entity-beneficial-owner.md) | `GET /company/:company_number/persons-with-significant-control/corporate-entity-beneficial-owner/:psc_id` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/persons-with-significant-control/corporate-entity-beneficial-owner/get) |
| [Get Company PSC Individual](actions/get-company-psc-individual.md) | `GET /company/:company_number/persons-with-significant-control/individual/:psc_id` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/persons-with-significant-control/individual/get) |
| [Get Company PSC Individual Beneficial Owner](actions/get-company-psc-individual-beneficial-owner.md) | `GET /company/:company_number/persons-with-significant-control/individual-beneficial-owner/:psc_id` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/persons-with-significant-control/individual-beneficial-owner/get) |
| [Get Company PSC Legal Person](actions/get-company-psc-legal-person.md) | `GET /company/:company_number/persons-with-significant-control/legal-person/:psc_id` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/persons-with-significant-control/legal-person/get) |
| [Get Company PSC Legal Person Beneficial Owner](actions/get-company-psc-legal-person-beneficial-owner.md) | `GET /company/:company_number/persons-with-significant-control/legal-person-beneficial-owner/:psc_id` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/persons-with-significant-control/legal-person-beneficial-owner/get) |
| [Get Company PSC Statement](actions/get-company-psc-statement.md) | `GET /company/:company_number/persons-with-significant-control-statements/:statement_id` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/persons-with-significant-control-statements/get) |
| [Get Company PSC Super Secure](actions/get-company-psc-super-secure.md) | `GET /company/:company_number/persons-with-significant-control/super-secure/:super_secure_id` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/persons-with-significant-control/super-secure/get) |
| [Get Company PSC Super Secure Beneficial Owner](actions/get-company-psc-super-secure-beneficial-owner.md) | `GET /company/:company_number/persons-with-significant-control/super-secure-beneficial-owner/:super_secure_id` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/persons-with-significant-control/super-secure-beneficial-owner/get) |
| [Get Disqualified Corporate Officer](actions/get-disqualified-corporate-officer.md) | `GET /disqualified-officers/corporate/:officer_id` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/disqualified-officer-corporate/get) |
| [Get Disqualified Natural Officer](actions/get-disqualified-natural-officer.md) | `GET /disqualified-officers/natural/:officer_id` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/disqualified-officer-natural/get) |
| [Get Registered Office Address](actions/get-registered-office-address.md) | `GET /company/:company_number/registered-office-address` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/registered-office-address) |
| [List Company Charges](actions/list-company-charges.md) | `GET /company/:company_number/charges` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/charges/list) |
| [List Company Filing History](actions/list-company-filing-history.md) | `GET /company/:company_number/filing-history` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/filing-history/list) |
| [List Company Officers](actions/list-company-officers.md) | `GET /company/:company_number/officers` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/officers/list) |
| [List Company PSC Statements](actions/list-company-psc-statements.md) | `GET /company/:company_number/persons-with-significant-control-statements` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/persons-with-significant-control-statements/list) |
| [List Company PSCs](actions/list-company-pscs.md) | `GET /company/:company_number/persons-with-significant-control` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/persons-with-significant-control/list) |
| [List Company Registers](actions/list-company-registers.md) | `GET /company/:company_number/registers` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/registers/list) |
| [List Company UK Establishments](actions/list-company-uk-establishments.md) | `GET /company/:company_number/uk-establishments` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/uk-establishments/list) |
| [List Officer Appointments](actions/list-officer-appointments.md) | `GET /officers/:officer_id/appointments` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/officers/appointments/list) |
| [Search All](actions/search-all.md) | `GET /search` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/search-all) |
| [Search Companies](actions/search-companies.md) | `GET /search/companies` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/search-companies) |
| [Search Companies Advanced](actions/search-companies-advanced.md) | `GET /advanced-search/companies` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/search-companies) |
| [Search Companies Alphabetically](actions/search-companies-alphabetically.md) | `GET /alphabetical-search/companies` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/search-companies) |
| [Search Disqualified Officers](actions/search-disqualified-officers.md) | `GET /search/disqualified-officers` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/search-disqualified-officers) |
| [Search Dissolved Companies](actions/search-dissolved-companies.md) | `GET /dissolved-search/companies` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/search-companies) |
| [Search Officers](actions/search-officers.md) | `GET /search/officers` | [docs](https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference/search-officers) |
