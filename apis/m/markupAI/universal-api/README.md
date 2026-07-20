# <img src="https://images.mindcloud.co/apps/icons/cropped-markupai-favicon-32x32_1774459129220.png" alt="Markup AI logo" width="28" height="28"> Markup AI: Universal API

Check content against style guides and rewrite copy to match brand, tone, and terminology.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/markupAI/latest
- **Category:** Marketing
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://markup.ai/
- **Vendor API docs:** https://docs.markup.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Style Guides](actions/list-style-guides.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/markupAI/latest/actions/list-style-guides?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Policies

| Action | Method | Description |
| --- | --- | --- |
| [Create Domain](actions/create-domain.md) | POST | Creates a new terminology domain in Markup AI. |
| [Create Style Guide](actions/create-style-guide.md) | POST | Creates a new style guide in Markup AI. |
| [Create Term](actions/create-term.md) | POST | Creates a new term in Markup AI. |
| [Create Term Set](actions/create-term-set.md) | POST | Creates a new term set in Markup AI. |
| [Delete Domain](actions/delete-domain.md) | DELETE | Deletes an existing terminology domain from Markup AI. |
| [Delete Style Guide](actions/delete-style-guide.md) | DELETE | Deletes an existing style guide from Markup AI. |
| [Delete Term](actions/delete-term.md) | DELETE | Deletes an existing term from Markup AI. |
| [Delete Term Set](actions/delete-term-set.md) | DELETE | Deletes an existing term set from Markup AI. |
| [Get Domain](actions/get-domain.md) | GET | Retrieves terminology domain details from Markup AI. |
| [Get Style Guide](actions/get-style-guide.md) | GET | Retrieves style guide details from Markup AI. |
| [Get Term](actions/get-term.md) | GET | Retrieves term details from Markup AI. |
| [Get Term Set](actions/get-term-set.md) | GET | Retrieves term set details from Markup AI. |
| [List Domains](actions/list-domains.md) | GET | Retrieves terminology domains from Markup AI. |
| [List Style Guides](actions/list-style-guides.md) | GET | Retrieves style guides from Markup AI. |
| [List Term Sets](actions/list-term-sets.md) | GET | Retrieves term sets from Markup AI. |
| [Search Terminology](actions/search-terminology.md) | GET | Finds terminology in Markup AI by search term. |
| [Update Domain](actions/update-domain.md) | PUT | Updates an existing terminology domain in Markup AI. |
| [Update Style Guide](actions/update-style-guide.md) | PUT | Updates an existing style guide in Markup AI. |
| [Update Term](actions/update-term.md) | PUT | Updates an existing term in Markup AI. |
| [Update Term Set](actions/update-term-set.md) | PUT | Updates an existing term set in Markup AI. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Create Style Check](actions/create-style-check.md) | POST | Creates a style check in Markup AI. |
| [Create Style Rewrite](actions/create-style-rewrite.md) | POST | Creates a style rewrite in Markup AI. |
| [Create Style Suggestion](actions/create-style-suggestion.md) | POST | Creates a style suggestion in Markup AI. |
| [Get Style Check](actions/get-style-check.md) | GET | Retrieves style check results from Markup AI. |
| [Get Style Rewrite](actions/get-style-rewrite.md) | GET | Retrieves style rewrite results from Markup AI. |
| [Get Style Suggestion](actions/get-style-suggestion.md) | GET | Retrieves style suggestion results from Markup AI. |

