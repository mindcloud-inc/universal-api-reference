# Snapchat Ads: Universal API

Create, manage, and report on Snapchat advertising objects including organizations, ad accounts, campaigns, ad squads, ads, creatives, media, targeting, pixels, and performance stats through the Snapchat Marketing API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/snapchatAdsApi/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://forbusiness.snapchat.com/advertising
- **Vendor API docs:** https://developers.snap.com/api/marketing-api/Ads-API/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Authenticated User](actions/get-authenticated-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/snapchatAdsApi/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Ad Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Ad Account](actions/get-ad-account.md) | GET | Retrieves an ad account from Snapchat Ads. |
| [List Ad Accounts](actions/list-ad-accounts.md) | GET | Retrieves ad accounts from Snapchat Ads. |
| [Update Ad Accounts](actions/update-ad-accounts.md) | PUT | Updates existing ad accounts in Snapchat Ads. |

### Ad Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaigns](actions/create-campaigns.md) | POST | Creates new campaigns in Snapchat Ads. |
| [Delete Campaign](actions/delete-campaign.md) | DELETE | Deletes an existing campaign from Snapchat Ads. |
| [Fetch Campaigns by IDs](actions/fetch-campaigns-by-ids.md) | GET | Retrieves campaigns from Snapchat Ads by campaign IDs. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Snapchat Ads. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Snapchat Ads. |
| [Update Campaigns](actions/update-campaigns.md) | PUT | Updates existing campaigns in Snapchat Ads. |

### Ad Squad

| Action | Method | Description |
| --- | --- | --- |
| [Create Ad Squads](actions/create-ad-squads.md) | POST | Creates new ad squads in Snapchat Ads. |
| [Delete Ad Squad](actions/delete-ad-squad.md) | DELETE | Deletes an existing ad squad from Snapchat Ads. |
| [Fetch Ad Squads by IDs](actions/fetch-ad-squads-by-ids.md) | GET | Retrieves ad squads from Snapchat Ads by ad squad IDs. |
| [Get Ad Squad](actions/get-ad-squad.md) | GET | Retrieves an ad squad from Snapchat Ads. |
| [List Ad Squads by Ad Account](actions/list-ad-squads-by-ad-account.md) | GET | Retrieves ad squads from Snapchat Ads by ad account. |
| [List Ad Squads by Campaign](actions/list-ad-squads-by-campaign.md) | GET | Retrieves ad squads from Snapchat Ads by campaign. |
| [Update Ad Squads](actions/update-ad-squads.md) | PUT | Updates existing ad squads in Snapchat Ads. |

### Ads

| Action | Method | Description |
| --- | --- | --- |
| [Create Ads](actions/create-ads.md) | POST | Creates new ads in Snapchat Ads. |
| [Delete Ad](actions/delete-ad.md) | DELETE | Deletes an existing ad from Snapchat Ads. |
| [Fetch Ads by IDs](actions/fetch-ads-by-ids.md) | GET | Retrieves ads from Snapchat Ads by ad IDs. |
| [Get Ad](actions/get-ad.md) | GET | Retrieves an ad from Snapchat Ads. |
| [List Ads by Ad Account](actions/list-ads-by-ad-account.md) | GET | Retrieves ads from Snapchat Ads by ad account. |
| [List Ads by Ad Squad](actions/list-ads-by-ad-squad.md) | GET | Retrieves ads from Snapchat Ads by ad squad. |
| [List Ads by Campaign](actions/list-ads-by-campaign.md) | GET | Retrieves ads from Snapchat Ads by campaign. |
| [Update Ads](actions/update-ads.md) | PUT | Updates existing ads in Snapchat Ads. |

### Billing Center

| Action | Method | Description |
| --- | --- | --- |
| [Get Billing Center](actions/get-billing-center.md) | GET | Retrieves a billing center from Snapchat Ads. |
| [List Billing Centers](actions/list-billing-centers.md) | GET | Retrieves billing centers from Snapchat Ads. |

### Creative Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Creatives](actions/create-creatives.md) | POST | Creates new creatives in Snapchat Ads. |
| [Fetch Creatives by IDs](actions/fetch-creatives-by-ids.md) | GET | Retrieves creatives from Snapchat Ads by creative IDs. |
| [Get Creative](actions/get-creative.md) | GET | Retrieves a creative from Snapchat Ads. |
| [List Creatives](actions/list-creatives.md) | GET | Retrieves creatives from Snapchat Ads. |

### Funding Source

| Action | Method | Description |
| --- | --- | --- |
| [Get Funding Source](actions/get-funding-source.md) | GET | Retrieves a funding source from Snapchat Ads. |
| [List Funding Sources](actions/list-funding-sources.md) | GET | Retrieves funding sources from Snapchat Ads. |

### Media

| Action | Method | Description |
| --- | --- | --- |
| [Create Media](actions/create-media.md) | POST | Creates new media assets in Snapchat Ads. |
| [Fetch Media by IDs](actions/fetch-media-by-ids.md) | GET | Retrieves media assets from Snapchat Ads by media IDs. |
| [Get Media](actions/get-media.md) | GET | Retrieves a media asset from Snapchat Ads. |
| [List Media](actions/list-media.md) | GET | Retrieves media assets from Snapchat Ads. |

### Metrics

| Action | Method | Description |
| --- | --- | --- |
| [Get Ad Account Stats](actions/get-ad-account-stats.md) | GET | Retrieves ad account performance stats from Snapchat Ads. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Snapchat Ads. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves organizations from Snapchat Ads. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Authenticated User](actions/get-authenticated-user.md) | GET | Retrieves the authenticated Snapchat Ads user. |

