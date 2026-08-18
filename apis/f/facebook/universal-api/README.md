# <img src="https://images.mindcloud.co/apps/icons/facebook_1782742775472.png" alt="Facebook logo" width="28" height="28"> Facebook: Universal API

Facebook through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/facebook/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Ad Campaign Query](actions/ad-campaign-query.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/facebook/latest/actions/ad-campaign-query?connectionId=$CONNECTION_ID&accountID=act_112816323599903" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Ad Campaign Query](actions/ad-campaign-query.md) | GET |  |
| [Get Page Ratings](actions/get-page-ratings.md) | GET |  |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Owned Pages](actions/get-owned-pages.md) | GET |  |

