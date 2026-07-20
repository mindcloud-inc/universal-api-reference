# <img src="https://images.mindcloud.co/apps/icons/foreplay_1774987982258.png" alt="Foreplay logo" width="28" height="28"> Foreplay: Universal API

Search, filter, and analyze Foreplay ads, brands, boards, swipefile, and usage data through the Foreplay Public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/foreplay/latest
- **Category:** Marketing / Advertising
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.foreplay.co
- **Vendor API docs:** https://docs.foreplay.co/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Usage](actions/get-usage.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/foreplay/latest/actions/get-usage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Ad

| Action | Method | Description |
| --- | --- | --- |
| [Get Ad](actions/get-ad.md) | GET | Retrieves a Foreplay ad by public ad ID. |
| [Get Ad by ID](actions/get-ad-by-id.md) | GET | Retrieves a Foreplay ad by internal ID. |
| [List Ad Duplicates](actions/list-ad-duplicates.md) | GET | Retrieves ads in Foreplay sharing an ad's creative. |
| [List Board Ads](actions/list-board-ads.md) | GET | Retrieves ads from a specific Foreplay board. |
| [List Brand Ads by Brand ID](actions/list-brand-ads-by-brand-id.md) | GET | Retrieves ads for one or more Foreplay brand IDs. |
| [List Brand Ads by Page ID](actions/list-brand-ads-by-page-id.md) | GET | Retrieves ads for a Facebook page ID in Foreplay. |
| [List Spyder Brand Ads](actions/list-spyder-brand-ads.md) | GET | Retrieves ads for a tracked Spyder brand in Foreplay. |
| [List Swipefile Ads](actions/list-swipefile-ads.md) | GET | Retrieves your saved swipefile ads from Foreplay. |
| [Search Discovery Ads](actions/search-discovery-ads.md) | GET | Finds ads in Foreplay's discovery index. |

### Board

| Action | Method | Description |
| --- | --- | --- |
| [List Boards](actions/list-boards.md) | GET | Retrieves your accessible boards from Foreplay. |

### Brand

| Action | Method | Description |
| --- | --- | --- |
| [Discover Brands by Ads](actions/discover-brands-by-ads.md) | GET | Finds brands in Foreplay by ad characteristics. |
| [Get Spyder Brand](actions/get-spyder-brand.md) | GET | Retrieves a tracked Spyder brand from Foreplay. |
| [List Board Brands](actions/list-board-brands.md) | GET | Retrieves brands from a specific Foreplay board. |
| [List Brands by Domain](actions/list-brands-by-domain.md) | GET | Finds Foreplay brands by advertising domain. |
| [List Spyder Brands](actions/list-spyder-brands.md) | GET | Retrieves your tracked Spyder brands from Foreplay. |
| [Search Discovery Brands](actions/search-discovery-brands.md) | GET | Finds brands in Foreplay's discovery index. |

### Brand Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Brand Analytics](actions/get-brand-analytics.md) | GET | Retrieves brand analytics data from Foreplay. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET | Retrieves your Foreplay account usage details. |

