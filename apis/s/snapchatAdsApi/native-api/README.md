# Snapchat Ads: Native API Reference

A consolidated summary of Snapchat Ads's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developers.snap.com/api/marketing-api/Ads-API/introduction
- **API base URL:** `https://adsapi.snapchat.com/v1`

## Authentication

### OAuth2

Authenticate with a Snapchat Marketing API OAuth app and authorize MindCloud to act on behalf of a Snapchat business user.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.snapchat.com/login/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.snapchat.com/login/oauth2/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `snapchat-marketing-api`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.snapchat.com/login/oauth2/access_token.

[Official authentication documentation](https://developers.snap.com/api/marketing-api/Ads-API/authentication)

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 50–1000). Use `cursor` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Ad Squads](actions/create-ad-squads.md) | `POST /campaigns/:campaignId/adsquads` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ad-squads) |
| [Create Ads](actions/create-ads.md) | `POST /adsquads/:adSquadId/ads` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ads) |
| [Create Campaigns](actions/create-campaigns.md) | `POST /adaccounts/:adAccountId/campaigns` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/campaigns) |
| [Create Creatives](actions/create-creatives.md) | `POST /adaccounts/:adAccountId/creatives` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/creatives) |
| [Create Media](actions/create-media.md) | `POST /adaccounts/:adAccountId/media` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/media) |
| [Delete Ad](actions/delete-ad.md) | `DELETE /ads/:adId` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ads) |
| [Delete Ad Squad](actions/delete-ad-squad.md) | `DELETE /adsquads/:adSquadId` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ad-squads) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /campaigns/:campaignId` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/campaigns) |
| [Fetch Ad Squads by IDs](actions/fetch-ad-squads-by-ids.md) | `POST /adaccounts/:adAccountId/get_adsquads_by_ids` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ad-squads) |
| [Fetch Ads by IDs](actions/fetch-ads-by-ids.md) | `POST /adaccounts/:adAccountId/get_ads_by_ids` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ads) |
| [Fetch Campaigns by IDs](actions/fetch-campaigns-by-ids.md) | `POST /adaccounts/:adAccountId/get_campaigns_by_ids` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/campaigns) |
| [Fetch Creatives by IDs](actions/fetch-creatives-by-ids.md) | `POST /adaccounts/:adAccountId/get_creatives_by_ids` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/creatives) |
| [Fetch Media by IDs](actions/fetch-media-by-ids.md) | `POST /adaccounts/:adAccountId/get_media_by_ids` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/media) |
| [Get Ad](actions/get-ad.md) | `GET /ads/:adId` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ads) |
| [Get Ad Account](actions/get-ad-account.md) | `GET /adaccounts/:adAccountId` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ad-accounts) |
| [Get Ad Account Stats](actions/get-ad-account-stats.md) | `GET /adaccounts/:adAccountId/stats` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/measurement) |
| [Get Ad Squad](actions/get-ad-squad.md) | `GET /adsquads/:adSquadId` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ad-squads) |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /me` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/user) |
| [Get Billing Center](actions/get-billing-center.md) | `GET /billingcenters/:billingCenterId` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/billing-centers) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:campaignId` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/campaigns) |
| [Get Creative](actions/get-creative.md) | `GET /creatives/:creativeId` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/creatives) |
| [Get Funding Source](actions/get-funding-source.md) | `GET /fundingsources/:fundingSourceId` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/funding-sources) |
| [Get Media](actions/get-media.md) | `GET /media/:mediaId` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/media) |
| [Get Organization](actions/get-organization.md) | `GET /organizations/:organizationId` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/organizations) |
| [List Ad Accounts](actions/list-ad-accounts.md) | `GET /organizations/:organizationId/adaccounts` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ad-accounts) |
| [List Ad Squads by Ad Account](actions/list-ad-squads-by-ad-account.md) | `GET /adaccounts/:adAccountId/adsquads` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ad-squads) |
| [List Ad Squads by Campaign](actions/list-ad-squads-by-campaign.md) | `GET /campaigns/:campaignId/adsquads` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ad-squads) |
| [List Ads by Ad Account](actions/list-ads-by-ad-account.md) | `GET /adaccounts/:adAccountId/ads` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ads) |
| [List Ads by Ad Squad](actions/list-ads-by-ad-squad.md) | `GET /adsquads/:adSquadId/ads` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ads) |
| [List Ads by Campaign](actions/list-ads-by-campaign.md) | `GET /campaigns/:campaignId/ads` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ads) |
| [List Billing Centers](actions/list-billing-centers.md) | `GET /organizations/:organizationId/billingcenters` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/billing-centers) |
| [List Campaigns](actions/list-campaigns.md) | `GET /adaccounts/:adAccountId/campaigns` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/campaigns) |
| [List Creatives](actions/list-creatives.md) | `GET /adaccounts/:adAccountId/creatives` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/creatives) |
| [List Funding Sources](actions/list-funding-sources.md) | `GET /organizations/:organizationId/fundingsources` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/funding-sources) |
| [List Media](actions/list-media.md) | `GET /adaccounts/:adAccountId/media` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/media) |
| [List Organizations](actions/list-organizations.md) | `GET /me/organizations` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/organizations) |
| [Update Ad Accounts](actions/update-ad-accounts.md) | `PUT /organizations/:organizationId/adaccounts` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ad-accounts) |
| [Update Ad Squads](actions/update-ad-squads.md) | `PUT /campaigns/:campaignId/adsquads` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ad-squads) |
| [Update Ads](actions/update-ads.md) | `PUT /adsquads/:adSquadId/ads` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/ads) |
| [Update Campaigns](actions/update-campaigns.md) | `PUT /adaccounts/:adAccountId/campaigns` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/campaigns) |
