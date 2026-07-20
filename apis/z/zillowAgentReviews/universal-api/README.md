# <img src="https://images.mindcloud.co/apps/icons/zillow-agent-reviews_1776963187603.png" alt="Zillow Agent Reviews logo" width="28" height="28"> Zillow Agent Reviews: Universal API

Bridge-hosted Zillow Agent Reviews data access. Requires a Bridge account and access to the reviews dataset.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zillowAgentReviews/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zillowgroup.com/developers/api/agents/agent-reviews/
- **Vendor API docs:** https://bridgedataoutput.com/docs/platform

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List reviewees](actions/list-reviewees.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zillowAgentReviews/latest/actions/list-reviewees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Comments

| Action | Method | Description |
| --- | --- | --- |
| [List reviews](actions/list-reviews.md) | GET | Retrieves agent reviews from Zillow Agent Reviews. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List reviewees](actions/list-reviewees.md) | GET | Retrieves reviewees from Zillow Agent Reviews. |

