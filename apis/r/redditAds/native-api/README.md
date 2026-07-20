# Reddit Lead Ads: Native API Reference

A consolidated summary of Reddit Lead Ads's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://ads-api.reddit.com/docs/v3/
- **OpenAPI specification:** https://ads-api.reddit.com/api/v3/openapi.json
- **API base URL:** `https://ads-api.reddit.com/api/v3`

## Pagination

Use `page.size` in the query string to set the page size (default 100; accepted range 1–1000). Use `page.token` in the query string as the pagination cursor. Follow the complete next-page URL returned by the API.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Ad](actions/create-ad.md) | `POST /ad_accounts/{ad_account_id}/ads` | [docs](https://ads-api.reddit.com/docs/v3/operations/create-ad) |
| [Create Ad Group](actions/create-ad-group.md) | `POST /ad_accounts/{ad_account_id}/ad_groups` | [docs](https://ads-api.reddit.com/docs/v3/operations/create-ad-group) |
| [Create Campaign](actions/create-campaign.md) | `POST /ad_accounts/{ad_account_id}/campaigns` | [docs](https://ads-api.reddit.com/docs/v3/operations/create-campaign) |
| [Create Custom Audience](actions/create-custom-audience.md) | `POST /ad_accounts/{ad_account_id}/custom_audiences` | [docs](https://ads-api.reddit.com/docs/v3/operations/create-custom-audience) |
| [Create Lead Gen Form](actions/create-lead-gen-form.md) | `POST /ad_accounts/{ad_account_id}/lead_gen_forms` | [docs](https://ads-api.reddit.com/docs/v3/operations/create-lead-gen-form) |
| [Create Saved Audience](actions/create-saved-audience.md) | `POST /ad_accounts/{ad_account_id}/saved_audiences` | [docs](https://ads-api.reddit.com/docs/v3/operations/create-saved-audience) |
| [Get A Report](actions/get-a-report.md) | `POST /ad_accounts/{ad_account_id}/reports` | [docs](https://ads-api.reddit.com/docs/v3/operations/get-a-report) |
| [Get Ad](actions/get-ad.md) | `GET /ads/{ad_id}` | [docs](https://ads-api.reddit.com/docs/v3/operations/get-ad) |
| [Get Ad Account](actions/get-ad-account.md) | `GET /ad_accounts/{ad_account_id}` | [docs](https://ads-api.reddit.com/docs/v3/operations/get-ad-account) |
| [Get Ad Account History](actions/get-ad-account-history.md) | `POST /ad_accounts/{ad_account_id}/history` | [docs](https://ads-api.reddit.com/docs/v3/operations/get-ad-account-history) |
| [Get Ad Group](actions/get-ad-group.md) | `GET /ad_groups/{ad_group_id}` | [docs](https://ads-api.reddit.com/docs/v3/operations/get-ad-group) |
| [Get Business](actions/get-business.md) | `GET /businesses/{business_id}` | [docs](https://ads-api.reddit.com/docs/v3/operations/get-business) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/{campaign_id}` | [docs](https://ads-api.reddit.com/docs/v3/operations/get-campaign) |
| [Get Custom Audience](actions/get-custom-audience.md) | `GET /custom_audiences/{audience_id}` | [docs](https://ads-api.reddit.com/docs/v3/operations/get-custom-audience) |
| [Get Last Fired At](actions/get-last-fired-at.md) | `GET /pixels/{pixel_id}/last_fired_at` | [docs](https://ads-api.reddit.com/docs/v3/operations/get-last-fired-at) |
| [Get Lead Gen Form](actions/get-lead-gen-form.md) | `GET /lead_gen_forms/{lead_gen_form_id}` | [docs](https://ads-api.reddit.com/docs/v3/operations/get-lead-gen-form) |
| [Get Me](actions/get-me.md) | `GET /me` | [docs](https://ads-api.reddit.com/docs/v3/operations/get-me) |
| [Get Saved Audience](actions/get-saved-audience.md) | `GET /saved_audiences/{saved_audience_id}` | [docs](https://ads-api.reddit.com/docs/v3/operations/get-saved-audience) |
| [List Ad Accounts By Business](actions/list-ad-accounts-by-business.md) | `GET /businesses/{business_id}/ad_accounts` | [docs](https://ads-api.reddit.com/docs/v3/operations/list-ad-accounts-by-business) |
| [List Ad Groups](actions/list-ad-groups.md) | `GET /ad_accounts/{ad_account_id}/ad_groups` | [docs](https://ads-api.reddit.com/docs/v3/operations/list-ad-groups) |
| [List Ads](actions/list-ads.md) | `GET /ad_accounts/{ad_account_id}/ads` | [docs](https://ads-api.reddit.com/docs/v3/operations/list-ads) |
| [List Campaigns](actions/list-campaigns.md) | `GET /ad_accounts/{ad_account_id}/campaigns` | [docs](https://ads-api.reddit.com/docs/v3/operations/list-campaigns) |
| [List Devices](actions/list-devices.md) | `GET /targeting/devices` | [docs](https://ads-api.reddit.com/docs/v3/operations/list-devices) |
| [List Geolocations](actions/list-geolocations.md) | `GET /targeting/geolocations` | [docs](https://ads-api.reddit.com/docs/v3/operations/list-geolocations) |
| [List Interests](actions/list-interests.md) | `GET /targeting/interests` | [docs](https://ads-api.reddit.com/docs/v3/operations/list-interests) |
| [List Keyword Suggestions](actions/list-keyword-suggestions.md) | `POST /targeting/keyword_suggestions` | [docs](https://ads-api.reddit.com/docs/v3/operations/list-keyword-suggestions) |
| [List Lead Gen Forms](actions/list-lead-gen-forms.md) | `GET /ad_accounts/{ad_account_id}/lead_gen_forms` | [docs](https://ads-api.reddit.com/docs/v3/operations/list-lead-gen-forms) |
| [List My Businesses](actions/list-my-businesses.md) | `GET /me/businesses` | [docs](https://ads-api.reddit.com/docs/v3/operations/list-my-businesses) |
| [List Pixels By Ad Account](actions/list-pixels-by-ad-account.md) | `GET /ad_accounts/{ad_account_id}/pixels` | [docs](https://ads-api.reddit.com/docs/v3/operations/list-pixels-by-ad-account) |
| [List Pixels By Business](actions/list-pixels-by-business.md) | `GET /businesses/{business_id}/pixels` | [docs](https://ads-api.reddit.com/docs/v3/operations/list-pixels-by-business) |
| [List Saved Audiences](actions/list-saved-audiences.md) | `GET /ad_accounts/{ad_account_id}/saved_audiences` | [docs](https://ads-api.reddit.com/docs/v3/operations/list-saved-audiences) |
| [List User Custom Audiences](actions/list-user-custom-audiences.md) | `GET /ad_accounts/{ad_account_id}/custom_audiences` | [docs](https://ads-api.reddit.com/docs/v3/operations/list-user-custom-audiences) |
| [Post Conversion Events](actions/post-conversion-events.md) | `POST /pixels/{pixel_id}/conversion_events` | [docs](https://ads-api.reddit.com/docs/v3/operations/post-conversion-events) |
| [Query Ad Accounts](actions/query-ad-accounts.md) | `POST /businesses/{business_id}/ad_accounts/query` | [docs](https://ads-api.reddit.com/docs/v3/operations/query-ad-accounts) |
| [Search Communities](actions/search-communities.md) | `GET /targeting/communities/search` | [docs](https://ads-api.reddit.com/docs/v3/operations/search-communities) |
| [Update Ad](actions/update-ad.md) | `PATCH /ads/{ad_id}` | [docs](https://ads-api.reddit.com/docs/v3/operations/update-ad) |
| [Update Ad Group](actions/update-ad-group.md) | `PATCH /ad_groups/{ad_group_id}` | [docs](https://ads-api.reddit.com/docs/v3/operations/update-ad-group) |
| [Update Campaign](actions/update-campaign.md) | `PATCH /campaigns/{campaign_id}` | [docs](https://ads-api.reddit.com/docs/v3/operations/update-campaign) |
| [Update Custom Audience Users](actions/update-custom-audience-users.md) | `PATCH /custom_audiences/{audience_id}/users` | [docs](https://ads-api.reddit.com/docs/v3/operations/update-custom-audience-users) |
| [Update Saved Audience](actions/update-saved-audience.md) | `PATCH /saved_audiences/{saved_audience_id}` | [docs](https://ads-api.reddit.com/docs/v3/operations/update-saved-audience) |
