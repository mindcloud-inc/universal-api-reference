# <img src="https://images.mindcloud.co/apps/icons/idv-zj-fm-xtr-logos_1774464724184.png" alt="Dappier logo" width="28" height="28"> Dappier: Universal API

Search real-time web data and retrieve AI recommendations

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dappier/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://dappier.com/
- **Vendor API docs:** https://docs.dappier.com/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Real Time Data](actions/search-real-time-data.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dappier/latest/actions/search-real-time-data?connectionId=$CONNECTION_ID&aiModelId=am_01j06ytn18ejftedz6dyhz2b15&query=What%20is%20the%20weather%20in%20Austin%20today%3F" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Recommendation

| Action | Method | Description |
| --- | --- | --- |
| [Get AI Recommendations By Query](actions/get-ai-recommendations-by-query.md) | GET | Retrieves AI article recommendations from Dappier by query. |
| [Get Cat Care Recommendations](actions/get-cat-care-recommendations.md) | GET | Retrieves cat care article recommendations from Dappier. |
| [Get Domain-Constrained Recommendations](actions/get-domain-constrained-recommendations.md) | GET | Retrieves AI article recommendations from Dappier for a specified domain. |
| [Get Most Recent Recommendations](actions/get-most-recent-recommendations.md) | GET | Retrieves the most recent AI article recommendations from Dappier. |
| [Get Trending Recommendations](actions/get-trending-recommendations.md) | GET | Retrieves trending AI article recommendations from Dappier. |

### Search

| Action | Method | Description |
| --- | --- | --- |
| [Search Real Time Data](actions/search-real-time-data.md) | GET | Retrieves a real-time AI search response from Dappier. |

