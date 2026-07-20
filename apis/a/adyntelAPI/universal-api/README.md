# <img src="https://images.mindcloud.co/apps/icons/adyntel_1783966062060.png" alt="Adyntel logo" width="28" height="28"> Adyntel: Universal API

Adyntel provides ad intelligence endpoints for Facebook, Google, LinkedIn, TikTok, Google Shopping, and domain keyword analysis.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/adyntelAPI/latest
- **Category:** Marketing / Advertising
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.adyntel.com
- **Vendor API docs:** https://docs.adyntel.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Meta Ads by Keyword](actions/search-meta-ads-by-keyword.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/adyntelAPI/latest/actions/search-meta-ads-by-keyword?connectionId=$CONNECTION_ID&keyword=shopify" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Ads

| Action | Method | Description |
| --- | --- | --- |
| [Get TikTok Ad Details](actions/get-tik-tok-ad-details.md) | GET | Retrieves TikTok ad details from Adyntel by ad ID. |
| [List Facebook and Instagram Ads](actions/list-facebook-and-instagram-ads.md) | GET | Retrieves Facebook and Instagram ads from Adyntel by company or page. |
| [List Google Ads](actions/list-google-ads.md) | GET | Retrieves Google ads from Adyntel by company domain. |
| [List LinkedIn Ads](actions/list-linked-in-ads.md) | GET | Retrieves LinkedIn ads from Adyntel by company domain. |
| [Search LinkedIn Ads by Keyword](actions/search-linked-in-ads-by-keyword.md) | GET | Finds LinkedIn ads in Adyntel by keyword. |
| [Search Meta Ads by Keyword](actions/search-meta-ads-by-keyword.md) | GET | Finds Meta ads in Adyntel by keyword. |
| [Search TikTok Ads](actions/search-tik-tok-ads.md) | GET | Finds TikTok ads in Adyntel by keyword. |

### Domain Keywords

| Action | Method | Description |
| --- | --- | --- |
| [Get Domain Keywords](actions/get-domain-keywords.md) | GET | Retrieves paid and organic keywords for a domain in Adyntel. |

### Shopping Ads

| Action | Method | Description |
| --- | --- | --- |
| [Get Google Shopping Status](actions/get-google-shopping-status.md) | GET | Retrieves Google Shopping search results from Adyntel by search ID. |
| [List Google Shopping Ads](actions/list-google-shopping-ads.md) | GET | Starts a Google Shopping ad search in Adyntel by company domain. |

