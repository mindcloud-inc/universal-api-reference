# <img src="https://images.mindcloud.co/apps/icons/socitcom_1774900936901.png" alt="Société.com logo" width="28" height="28"> Société.com: Universal API

Search and retrieve French company legal, financial, officer, and document data from Société.com.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/socitcom/latest
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.societe.com/
- **Vendor API docs:** https://api.societe.com/apisite/documentations/v1/documentation-api.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Client Information](actions/get-client-information.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socitcom/latest/actions/get-client-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Client Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Client Information](actions/get-client-information.md) | GET | Retrieves client account information from Société.com. |

### Client Log

| Action | Method | Description |
| --- | --- | --- |
| [List Client Log](actions/list-client-log.md) | GET | Retrieves client API usage logs from Société.com. |

### Company Autocomplete Results

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Companies](actions/autocomplete-companies.md) | GET | Finds company autocomplete suggestions in Société.com. |

### Company Collective Procedures

| Action | Method | Description |
| --- | --- | --- |
| [List Company Collective Procedures](actions/list-company-collective-procedures.md) | GET | Retrieves company collective procedures from Société.com. |

### Company Contact

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Contact Details](actions/get-company-contact-details.md) | GET | Retrieves company contact details from Société.com. |

### Company Establishments

| Action | Method | Description |
| --- | --- | --- |
| [List Company Establishments](actions/list-company-establishments.md) | GET | Retrieves company establishments from Société.com. |

### Company Events

| Action | Method | Description |
| --- | --- | --- |
| [List Company Events](actions/list-company-events.md) | GET | Retrieves company events from Société.com. |

### Company Existence

| Action | Method | Description |
| --- | --- | --- |
| [Check Company Exists](actions/check-company-exists.md) | GET | Checks whether a company exists in Société.com. |

### Company Financial Statements

| Action | Method | Description |
| --- | --- | --- |
| [List Company Financial Statements](actions/list-company-financial-statements.md) | GET | Retrieves company financial statements from Société.com. |

### Company Legal Information

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Legal Information](actions/get-company-legal-information.md) | GET | Retrieves company legal information from Société.com. |

### Company Officers

| Action | Method | Description |
| --- | --- | --- |
| [List Company Officers](actions/list-company-officers.md) | GET | Retrieves company officers from Société.com. |

### Company Official Documents

| Action | Method | Description |
| --- | --- | --- |
| [List Company Official Documents](actions/list-company-official-documents.md) | GET | Retrieves company official documents from Société.com. |

### Company Scoring

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Scoring](actions/get-company-scoring.md) | GET | Retrieves company scoring from Société.com. |

### Company Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Search Companies](actions/search-companies.md) | GET | Finds companies in Société.com by company name. |

### Company Trademarks

| Action | Method | Description |
| --- | --- | --- |
| [List Company Trademarks](actions/list-company-trademarks.md) | GET | Retrieves company trademarks from Société.com. |

### Establishment Autocomplete Results

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Establishments](actions/autocomplete-establishments.md) | GET | Finds establishment autocomplete suggestions in Société.com. |

### Establishment Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Search Establishments](actions/search-establishments.md) | GET | Finds establishments in Société.com by company name. |

### Officer Autocomplete Results

| Action | Method | Description |
| --- | --- | --- |
| [Autocomplete Officers](actions/autocomplete-officers.md) | GET | Finds officer autocomplete suggestions in Société.com. |

### Officer Mandates

| Action | Method | Description |
| --- | --- | --- |
| [Get Officer Mandates](actions/get-officer-mandates.md) | GET | Retrieves officer mandates from Société.com. |

### Official Document Download

| Action | Method | Description |
| --- | --- | --- |
| [Download Official Document](actions/download-official-document.md) | GET | Downloads an official document from Société.com. |

