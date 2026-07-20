# <img src="https://images.mindcloud.co/apps/icons/humantic-ai_1776802598160.png" alt="Humantic AI logo" width="28" height="28"> Humantic AI: Universal API

Humantic AI provides personality and buyer-intelligence APIs for creating and fetching people intelligence profiles from LinkedIn URLs, email addresses, documents, and free-form text.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/humanticAI/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 5
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://humantic.ai/
- **Vendor API docs:** https://api.humantic.ai/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Fetch Analysis](actions/fetch-analysis.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/humanticAI/latest/actions/fetch-analysis?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (5)

### Document Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Create Document Analysis](actions/create-document-analysis.md) | POST |  |

### Text Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Create Text Analysis](actions/create-text-analysis.md) | POST |  |

### User Profile Analysis

| Action | Method | Description |
| --- | --- | --- |
| [Create Profile Analysis](actions/create-profile-analysis.md) | POST |  |
| [Fetch Analysis](actions/fetch-analysis.md) | GET |  |
| [Update Analysis With Text](actions/update-analysis-with-text.md) | PUT |  |

