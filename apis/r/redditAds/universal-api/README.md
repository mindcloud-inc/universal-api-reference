# <img src="https://images.mindcloud.co/apps/icons/reddit-ads_1776112606855.png" alt="Reddit Lead Ads logo" width="28" height="28"> Reddit Lead Ads: Universal API

Manage Reddit campaigns, audiences, lead forms, pixels, and reports

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/redditAds/latest
- **Category:** Marketing
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ads.reddit.com/
- **Vendor API docs:** https://ads-api.reddit.com/docs/v3/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Me](actions/get-me.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redditAds/latest/actions/get-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Ad

| Action | Method | Description |
| --- | --- | --- |
| [Create Ad](actions/create-ad.md) | POST | Creates an ad in Reddit Ads. |
| [Get Ad](actions/get-ad.md) | GET | Retrieves an ad from Reddit Ads. |
| [List Ads](actions/list-ads.md) | GET | Retrieves ads for an ad account from Reddit Ads. |
| [Update Ad](actions/update-ad.md) | PUT | Updates an ad in Reddit Ads. |

### Ad Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Ad Account](actions/get-ad-account.md) | GET | Retrieves an ad account from Reddit Ads. |
| [List Ad Accounts By Business](actions/list-ad-accounts-by-business.md) | GET | Retrieves ad accounts for a business from Reddit Ads. |
| [Query Ad Accounts](actions/query-ad-accounts.md) | GET | Finds ad accounts for a business in Reddit Ads. |

### Ad Account History

| Action | Method | Description |
| --- | --- | --- |
| [Get Ad Account History](actions/get-ad-account-history.md) | GET | Retrieves the changelog for an ad account in Reddit Ads. |

### Ad Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Ad Group](actions/create-ad-group.md) | POST | Creates an ad group in Reddit Ads. |
| [Get Ad Group](actions/get-ad-group.md) | GET | Retrieves an ad group from Reddit Ads. |
| [List Ad Groups](actions/list-ad-groups.md) | GET | Retrieves ad groups for an ad account from Reddit Ads. |
| [Update Ad Group](actions/update-ad-group.md) | PUT | Updates an ad group in Reddit Ads. |

### Business

| Action | Method | Description |
| --- | --- | --- |
| [Get Business](actions/get-business.md) | GET | Retrieves a business from Reddit Ads. |
| [List My Businesses](actions/list-my-businesses.md) | GET | Retrieves businesses for the authenticated user from Reddit Ads. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a campaign in Reddit Ads. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Reddit Ads. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns for an ad account from Reddit Ads. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates a campaign in Reddit Ads. |

### Community

| Action | Method | Description |
| --- | --- | --- |
| [Search Communities](actions/search-communities.md) | GET | Finds targetable communities in Reddit Ads by name or topic. |

### Conversion Event

| Action | Method | Description |
| --- | --- | --- |
| [Post Conversion Events](actions/post-conversion-events.md) | POST | Creates conversion events for a Reddit pixel. |

### Custom Audience

| Action | Method | Description |
| --- | --- | --- |
| [Create Custom Audience](actions/create-custom-audience.md) | POST | Creates a custom audience in Reddit Ads. |
| [Get Custom Audience](actions/get-custom-audience.md) | GET | Retrieves a custom audience from Reddit Ads. |
| [List User Custom Audiences](actions/list-user-custom-audiences.md) | GET | Retrieves custom audiences for an ad account from Reddit Ads. |
| [Update Custom Audience Users](actions/update-custom-audience-users.md) | PUT | Updates users in a custom audience in Reddit Ads. |

### Device

| Action | Method | Description |
| --- | --- | --- |
| [List Devices](actions/list-devices.md) | GET | Retrieves targetable devices from Reddit Ads. |

### Geolocation

| Action | Method | Description |
| --- | --- | --- |
| [List Geolocations](actions/list-geolocations.md) | GET | Retrieves targetable geolocations from Reddit Ads. |

### Interest

| Action | Method | Description |
| --- | --- | --- |
| [List Interests](actions/list-interests.md) | GET | Retrieves targetable interests from Reddit Ads. |

### Keyword Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [List Keyword Suggestions](actions/list-keyword-suggestions.md) | GET | Retrieves keyword suggestions from input terms in Reddit Ads. |

### Lead Gen Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead Gen Form](actions/create-lead-gen-form.md) | POST | Creates a lead generation form in Reddit Ads. |
| [Get Lead Gen Form](actions/get-lead-gen-form.md) | GET | Retrieves a lead generation form from Reddit Ads. |
| [List Lead Gen Forms](actions/list-lead-gen-forms.md) | GET | Retrieves lead generation forms from Reddit Ads. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [Get Me](actions/get-me.md) | GET | Retrieves the authenticated user from Reddit Ads. |

### Pixel

| Action | Method | Description |
| --- | --- | --- |
| [Get Last Fired At](actions/get-last-fired-at.md) | GET | Retrieves the last fired time for a Reddit pixel. |
| [List Pixels By Ad Account](actions/list-pixels-by-ad-account.md) | GET | Retrieves pixels for an ad account from Reddit Ads. |
| [List Pixels By Business](actions/list-pixels-by-business.md) | GET | Retrieves pixels for a business from Reddit Ads. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [Get A Report](actions/get-a-report.md) | GET | Generates a metrics report in Reddit Ads. |

### Saved Audience

| Action | Method | Description |
| --- | --- | --- |
| [Create Saved Audience](actions/create-saved-audience.md) | POST | Creates a saved audience in Reddit Ads. |
| [Get Saved Audience](actions/get-saved-audience.md) | GET | Retrieves a saved audience from Reddit Ads. |
| [List Saved Audiences](actions/list-saved-audiences.md) | GET | Retrieves saved audiences from Reddit Ads. |
| [Update Saved Audience](actions/update-saved-audience.md) | PUT | Updates a saved audience in Reddit Ads. |

