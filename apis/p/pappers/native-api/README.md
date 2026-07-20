# Pappers: Native API Reference

A consolidated summary of Pappers's API configuration and 16 documented operations, with links to official documentation.

- **Official docs:** https://www.pappers.fr/api/documentation
- **API base URL:** `https://api.pappers.fr/v2`

## Authentication

### API Token

### Credentials

- **API Key:** `apiKey` · required · Your Pappers API token.

[Official authentication documentation](https://www.pappers.fr/api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The current page number is read from `page`.

## Endpoints (16 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get API Usage](actions/get-api-usage.md) | `GET /suivi-jetons` | [docs](https://www.pappers.fr/api/documentation) |
| [Get Beneficial Ownership Declaration](actions/get-beneficial-ownership-declaration.md) | `GET /document/declaration_beneficiaires_effectifs` | [docs](https://www.pappers.fr/api/documentation) |
| [Get Company](actions/get-company.md) | `GET /entreprise` | [docs](https://www.pappers.fr/api/documentation) |
| [Get Company Accounts](actions/get-company-accounts.md) | `GET /entreprise/comptes` | [docs](https://www.pappers.fr/api/documentation) |
| [Get Company Map](actions/get-company-map.md) | `GET /entreprise/cartographie` | [docs](https://www.pappers.fr/api/documentation) |
| [Get Company Suggestions](actions/get-company-suggestions.md) | `GET /suggestions` | [docs](https://www.pappers.fr/api/documentation) |
| [Get Financial Report](actions/get-financial-report.md) | `GET /document/rapport_financier` | [docs](https://www.pappers.fr/api/documentation) |
| [Get INPI Extract](actions/get-inpi-extract.md) | `GET /document/extrait_inpi` | [docs](https://www.pappers.fr/api/documentation) |
| [Get INSEE Status Document](actions/get-insee-status-document.md) | `GET /document/avis_situation_insee` | [docs](https://www.pappers.fr/api/documentation) |
| [Get Latest Statutes](actions/get-latest-statutes.md) | `GET /document/statuts` | [docs](https://www.pappers.fr/api/documentation) |
| [Get Non-Financial Report](actions/get-non-financial-report.md) | `GET /document/rapport_non_financier` | [docs](https://www.pappers.fr/api/documentation) |
| [Get Pappers Extract](actions/get-pappers-extract.md) | `GET /document/extrait_pappers` | [docs](https://www.pappers.fr/api/documentation) |
| [Search Companies](actions/search-companies.md) | `GET /recherche` | [docs](https://www.pappers.fr/api/documentation) |
| [Search Directors](actions/search-directors.md) | `GET /recherche-dirigeants` | [docs](https://www.pappers.fr/api/documentation) |
| [Search Documents](actions/search-documents.md) | `GET /recherche-documents` | [docs](https://www.pappers.fr/api/documentation) |
| [Search Publications](actions/search-publications.md) | `GET /recherche-publications` | [docs](https://www.pappers.fr/api/documentation) |
