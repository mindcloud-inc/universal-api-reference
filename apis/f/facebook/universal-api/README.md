# <img src="https://images.mindcloud.co/apps/icons/facebook_1782742775472.png" alt="Facebook logo" width="28" height="28"> Facebook: Universal API

Connect Facebook Pages, Meta Business assets, and advertising data to workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/facebook/latest
- **Actions:** 8
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.facebook.com/business
- **Vendor API docs:** https://developers.facebook.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Pages](actions/list-pages.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/facebook/latest/actions/list-pages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (8)

### Accounts

| Action | Method | Description |
| --- | --- | --- |
| [List Ad Accounts](actions/list-ad-accounts.md) | GET | Retrieve a list of the advertising accounts to which the authenticated user has access. |
| [List Businesses](actions/list-businesses.md) | GET | Retrieve a list of the business accounts to which the authenticated user has access. |

### Ad Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Ad Campaign Query](actions/ad-campaign-query.md) | GET |  |

### Ads

| Action | Method | Description |
| --- | --- | --- |
| [Ad Account Ads Query](actions/ad-account-ads-query.md) | GET |  |

### Page

| Action | Method | Description |
| --- | --- | --- |
| [Get Page](actions/get-page.md) | GET |  |
| [List Pages](actions/list-pages.md) | GET | List pages you manage/own |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Owned Pages](actions/get-owned-pages.md) | GET | Retrieve a list of Pages owned by the specified business account. |
| [Get Page Insights](actions/get-page-insights.md) | GET | Get analytics and metrics for a Page. |

