# <img src="https://images.mindcloud.co/apps/icons/handelsregister-ai_1776088735876.png" alt="Handelsregister AI logo" width="28" height="28"> Handelsregister AI: Universal API

Search German commercial-register organizations, fetch company details, and retrieve official registry documents.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/handelsregisterAI/latest
- **Category:** IT Operations / Database
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://handelsregister.ai/
- **Vendor API docs:** https://handelsregister.ai/en/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Organizations](actions/search-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/handelsregisterAI/latest/actions/search-organizations?connectionId=$CONNECTION_ID&q=BMW%20AG" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Api Token

| Action | Method | Description |
| --- | --- | --- |
| [Create API Token](actions/create-api-token.md) | POST | Creates a new API token in Handelsregister AI. |
| [List API Tokens](actions/list-api-tokens.md) | GET | Retrieves a list of API tokens from Handelsregister AI. |
| [Revoke API Token](actions/revoke-api-token.md) | DELETE | Revokes an existing API token from Handelsregister AI. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Balance Sheet Accounts](actions/get-company-balance-sheet-accounts.md) | GET | Retrieves company balance sheet accounts from Handelsregister AI. |
| [Get Company Financial KPIs](actions/get-company-financial-kpis.md) | GET | Retrieves company financial KPIs from Handelsregister AI. |
| [Get Company Profile](actions/get-company-profile.md) | GET | Retrieves a company profile from Handelsregister AI. |
| [Get Company With AI Search](actions/get-company-with-ai-search.md) | GET | Retrieves a company using AI search in Handelsregister AI. |
| [Search Organizations](actions/search-organizations.md) | GET | Finds organizations in Handelsregister AI by search query. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Download Shareholders List Document](actions/download-shareholders-list-document.md) | GET | Retrieves a shareholders list document from Handelsregister AI. |

