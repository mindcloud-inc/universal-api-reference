# Société.com: Native API Reference

A consolidated summary of Société.com's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://api.societe.com/apisite/documentations/v1/documentation-api.html
- **API base URL:** `https://api.societe.com/api/v1`

## Authentication

### API Key

Société.com API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://back.api.societe.com/)

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Autocomplete Companies](actions/autocomplete-companies.md) | `GET /autocomplete/entreprise` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#recherche-autocomplete-entreprises-get) |
| [Autocomplete Establishments](actions/autocomplete-establishments.md) | `GET /autocomplete/etablissement` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#recherche-autocomplete-&eacute;tablissements-get) |
| [Autocomplete Officers](actions/autocomplete-officers.md) | `GET /autocomplete/dirigeant` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#recherche-autocomplete-dirigeants-get) |
| [Check Company Exists](actions/check-company-exists.md) | `GET /entreprise/:numid/exist` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-existence-get) |
| [Download Official Document](actions/download-official-document.md) | `GET /documents-officiels/:id/download` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-t&eacute;l&eacute;chargement-des-documents-officiels-get) |
| [Get Client Information](actions/get-client-information.md) | `GET /infoclient` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#compte-client-informations-client-get) |
| [Get Company Contact Details](actions/get-company-contact-details.md) | `GET /entreprise/:numid/contact` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-contact-get) |
| [Get Company Legal Information](actions/get-company-legal-information.md) | `GET /entreprise/:numid/infoslegales` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-informations-l&eacute;gales-get) |
| [Get Company Scoring](actions/get-company-scoring.md) | `GET /entreprise/:numid/scoring` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-scoring-get) |
| [Get Officer Mandates](actions/get-officer-mandates.md) | `GET /mandats/:dirid` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#dirigeant-cartographie-get) |
| [List Client Log](actions/list-client-log.md) | `GET /logclient` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#compte-client-log-client-get) |
| [List Company Collective Procedures](actions/list-company-collective-procedures.md) | `GET /entreprise/:numid/procedurescollectives` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-proc&eacute;dures-collectives-get) |
| [List Company Establishments](actions/list-company-establishments.md) | `GET /entreprise/:numid/etablissements` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-etablissements-get) |
| [List Company Events](actions/list-company-events.md) | `GET /entreprise/:numid/evenements` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-ev&egrave;nements-get) |
| [List Company Financial Statements](actions/list-company-financial-statements.md) | `GET /entreprise/:numid/bilans` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-bilans-get) |
| [List Company Officers](actions/list-company-officers.md) | `GET /entreprise/:numid/dirigeants` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-dirigeants-get) |
| [List Company Official Documents](actions/list-company-official-documents.md) | `GET /entreprise/:numid/documents-officiels` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-documents-officiels-get) |
| [List Company Trademarks](actions/list-company-trademarks.md) | `GET /entreprise/:numid/marques` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-marques-get) |
| [Search Companies](actions/search-companies.md) | `GET /entreprise/search` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#recherche-recherche-d-entreprise-get) |
| [Search Establishments](actions/search-establishments.md) | `GET /etablissement/search` | [docs](https://api.societe.com/apisite/documentations/v1/documentation-api.html#recherche-recherche-d-&eacute;tablissement-get) |
