# <img src="https://images.mindcloud.co/apps/icons/id-c-f-sr4f8-logos_1777316675851.png" alt="OpenRegister logo" width="28" height="28"> OpenRegister: Universal API

Search and enrich German company register data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/openRegister/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 16
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://openregister.de
- **Vendor API docs:** https://docs.openregister.de

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Advanced Company Search](actions/advanced-company-search.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openRegister/latest/actions/advanced-company-search?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (16)

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Advanced Company Search](actions/advanced-company-search.md) | GET | Finds companies in OpenRegister using advanced filters. |
| [Autocomplete Companies](actions/autocomplete-companies.md) | GET | Finds company matches in OpenRegister as you type. |
| [Get Company](actions/get-company.md) | GET | Retrieves company information from OpenRegister by company ID. |
| [Get Company Historical Owners](actions/get-company-historical-owners.md) | GET | Retrieves a company's historical owners from OpenRegister. |
| [Get Company Holdings](actions/get-company-holdings.md) | GET | Retrieves a company's holdings from OpenRegister. |
| [Get Company Owners](actions/get-company-owners.md) | GET | Retrieves a company's owners from OpenRegister. |
| [Get Company UBOs](actions/get-company-ubos.md) | GET | Retrieves a company's ultimate beneficial owners from OpenRegister. |
| [Get Person Holdings](actions/get-person-holdings.md) | GET | Retrieves a person's holdings from OpenRegister. |
| [Search Company By Website URL](actions/search-company-by-website-url.md) | GET | Finds a company in OpenRegister by website URL. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in OpenRegister by name or register details. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Contact Information](actions/get-company-contact-information.md) | GET | Retrieves a company's contact information from OpenRegister. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Realtime Document](actions/get-realtime-document.md) | GET | Retrieves a realtime company document from OpenRegister. |
| [Get Stored Document](actions/get-stored-document.md) | GET | Retrieves a stored document from OpenRegister by document ID. |

### Monitors

| Action | Method | Description |
| --- | --- | --- |
| [List Monitors](actions/list-monitors.md) | GET | Retrieves existing monitor records from OpenRegister. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Person](actions/get-person.md) | GET | Retrieves person information from OpenRegister by person ID. |
| [Search Persons](actions/search-persons.md) | GET | Finds people in OpenRegister using advanced filters. |

