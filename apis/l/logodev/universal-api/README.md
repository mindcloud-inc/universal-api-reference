# <img src="https://images.mindcloud.co/apps/icons/opengraph_1776193462769.png" alt="Logo.dev logo" width="28" height="28"> Logo.dev: Universal API

Find company logos and brand data by domain, name, or ticker

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/logodev/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.logo.dev
- **Vendor API docs:** https://www.logo.dev/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Company Domains](actions/search-company-domains.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logodev/latest/actions/search-company-domains?connectionId=$CONNECTION_ID&q=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Company Logo by Domain](actions/get-company-logo-by-domain.md) | GET | Retrieves a company logo from Logo.dev by domain. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Describe Company](actions/describe-company.md) | GET | Retrieves company details from Logo.dev by domain. |
| [Search Company Domains](actions/search-company-domains.md) | GET | Finds company domains in Logo.dev. |

