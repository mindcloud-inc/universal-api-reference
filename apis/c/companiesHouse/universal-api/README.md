# <img src="https://images.mindcloud.co/apps/icons/companies-house-source_1776432310183.png" alt="Companies House logo" width="28" height="28"> Companies House: Universal API

Read-only wrapper for the Companies House Public Data API, covering company search and retrieval endpoints for public UK company information.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/companiesHouse/latest
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://developer.company-information.service.gov.uk/
- **Vendor API docs:** https://developer-specs.company-information.service.gov.uk/companies-house-public-data-api/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Company Profile](actions/get-company-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-profile?connectionId=$CONNECTION_ID&companyNumber=00000006" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Address

| Action | Method | Description |
| --- | --- | --- |
| [Get Registered Office Address](actions/get-registered-office-address.md) | GET | Retrieves a registered office address from Companies House. |

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Officer Appointment](actions/get-company-officer-appointment.md) | GET | Retrieves a company officer appointment from Companies House. |
| [List Officer Appointments](actions/list-officer-appointments.md) | GET | Retrieves officer appointments from Companies House. |

### Charge

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Charge](actions/get-company-charge.md) | GET | Retrieves a company charge from Companies House. |
| [List Company Charges](actions/list-company-charges.md) | GET | Retrieves company charges from Companies House. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Profile](actions/get-company-profile.md) | GET | Retrieves a company profile from Companies House. |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in Companies House. |
| [Search Companies Advanced](actions/search-companies-advanced.md) | GET | Finds companies in Companies House by advanced filters. |
| [Search Companies Alphabetically](actions/search-companies-alphabetically.md) | GET | Finds companies in Companies House alphabetically. |
| [Search Dissolved Companies](actions/search-dissolved-companies.md) | GET | Finds dissolved companies in Companies House. |

### Company Exemptions

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Exemptions](actions/get-company-exemptions.md) | GET | Retrieves company exemptions from Companies House. |

### Disqualified Officer

| Action | Method | Description |
| --- | --- | --- |
| [Get Disqualified Corporate Officer](actions/get-disqualified-corporate-officer.md) | GET | Retrieves a disqualified corporate officer from Companies House. |
| [Get Disqualified Natural Officer](actions/get-disqualified-natural-officer.md) | GET | Retrieves a disqualified natural officer from Companies House. |
| [Search Disqualified Officers](actions/search-disqualified-officers.md) | GET | Finds disqualified officers in Companies House. |

### Filing History Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Filing History Item](actions/get-company-filing-history-item.md) | GET | Retrieves a company filing history item from Companies House. |
| [List Company Filing History](actions/list-company-filing-history.md) | GET | Retrieves company filing history from Companies House. |

### Insolvency

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Insolvency](actions/get-company-insolvency.md) | GET | Retrieves company insolvency details from Companies House. |

### Officer

| Action | Method | Description |
| --- | --- | --- |
| [List Company Officers](actions/list-company-officers.md) | GET | Retrieves company officers from Companies House. |
| [Search Officers](actions/search-officers.md) | GET | Finds officers in Companies House. |

### Psc

| Action | Method | Description |
| --- | --- | --- |
| [Get Company PSC Corporate Entity](actions/get-company-psc-corporate-entity.md) | GET | Retrieves a corporate entity with significant control notification from Companies House. |
| [Get Company PSC Corporate Entity Beneficial Owner](actions/get-company-psc-corporate-entity-beneficial-owner.md) | GET | Retrieves a corporate entity beneficial owner notification from Companies House. |
| [Get Company PSC Individual](actions/get-company-psc-individual.md) | GET | Retrieves an individual person with significant control notification from Companies House. |
| [Get Company PSC Individual Beneficial Owner](actions/get-company-psc-individual-beneficial-owner.md) | GET | Retrieves an individual beneficial owner notification from Companies House. |
| [Get Company PSC Legal Person](actions/get-company-psc-legal-person.md) | GET | Retrieves a legal person with significant control notification from Companies House. |
| [Get Company PSC Legal Person Beneficial Owner](actions/get-company-psc-legal-person-beneficial-owner.md) | GET | Retrieves a legal person beneficial owner notification from Companies House. |
| [Get Company PSC Super Secure](actions/get-company-psc-super-secure.md) | GET | Retrieves a super secure person with significant control from Companies House. |
| [Get Company PSC Super Secure Beneficial Owner](actions/get-company-psc-super-secure-beneficial-owner.md) | GET | Retrieves a super secure beneficial owner notification from Companies House. |
| [List Company PSCs](actions/list-company-pscs.md) | GET | Retrieves company persons with significant control from Companies House. |

### Psc Statement

| Action | Method | Description |
| --- | --- | --- |
| [Get Company PSC Statement](actions/get-company-psc-statement.md) | GET | Retrieves a person with significant control statement from Companies House. |
| [List Company PSC Statements](actions/list-company-psc-statements.md) | GET | Retrieves company persons with significant control statements from Companies House. |

### Register

| Action | Method | Description |
| --- | --- | --- |
| [List Company Registers](actions/list-company-registers.md) | GET | Retrieves company registers from Companies House. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search All](actions/search-all.md) | GET | Finds companies, officers, and disqualified officers in Companies House. |

### Uk Establishment

| Action | Method | Description |
| --- | --- | --- |
| [List Company UK Establishments](actions/list-company-uk-establishments.md) | GET | Retrieves company UK establishments from Companies House. |

