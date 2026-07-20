# <img src="https://images.mindcloud.co/apps/icons/linked-in-icon_1777325342659.png" alt="LinkedIn Ads Reports logo" width="28" height="28"> LinkedIn Ads Reports: Universal API

Retrieve LinkedIn Ads reporting, campaign structure, and related marketing analytics data from LinkedIn Marketing APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/linkedInAdsReports/latest
- **Category:** Marketing
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.linkedin.com
- **Vendor API docs:** https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads-reporting/ads-reporting?view=li-lms-2026-03

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Ad Analytics](actions/get-ad-analytics.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedInAdsReports/latest/actions/get-ad-analytics?connectionId=$CONNECTION_ID&pivot=ACCOUNT&facet=accounts%3DList(urn%253Ali%253AsponsoredAccount%253A123456)&startYear=2026&startMonth=4&startDay=1&endYear=2026&endMonth=4&endDay=26&timeGranularity=DAILY" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Ad Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Get Ad Account](actions/get-ad-account.md) | GET | Retrieves an ad account from LinkedIn Ads Reports. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from LinkedIn Ads Reports. |
| [Search Ad Accounts](actions/search-ad-accounts.md) | GET | Finds ad accounts in LinkedIn Ads Reports. |
| [Search Campaigns](actions/search-campaigns.md) | GET | Finds campaigns in LinkedIn Ads Reports. |

### Ad Groups

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Group](actions/get-campaign-group.md) | GET | Retrieves a campaign group from LinkedIn Ads Reports. |
| [Search Campaign Groups](actions/search-campaign-groups.md) | GET | Finds campaign groups in LinkedIn Ads Reports. |

### Ads

| Action | Method | Description |
| --- | --- | --- |
| [Get Creative](actions/get-creative.md) | GET | Retrieves a creative from LinkedIn Ads Reports. |
| [Search Creatives](actions/search-creatives.md) | GET | Finds creatives in LinkedIn Ads Reports. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Analytics](actions/get-account-analytics.md) | GET | Retrieves account analytics from LinkedIn Ads Reports. |
| [Get Ad Analytics](actions/get-ad-analytics.md) | GET | Retrieves ad analytics from LinkedIn Ads Reports. |
| [Get Ad Statistics](actions/get-ad-statistics.md) | GET | Retrieves ad statistics from LinkedIn Ads Reports. |
| [Get Campaign Analytics](actions/get-campaign-analytics.md) | GET | Retrieves campaign analytics from LinkedIn Ads Reports. |
| [Get Company Demographics](actions/get-company-demographics.md) | GET | Retrieves company demographics from LinkedIn Ads Reports. |
| [Get Country Demographics](actions/get-country-demographics.md) | GET | Retrieves country demographics from LinkedIn Ads Reports. |
| [Get Creative Analytics](actions/get-creative-analytics.md) | GET | Retrieves creative analytics from LinkedIn Ads Reports. |
| [Get Industry Demographics](actions/get-industry-demographics.md) | GET | Retrieves industry demographics from LinkedIn Ads Reports. |
| [Get Job Function Demographics](actions/get-job-function-demographics.md) | GET | Retrieves job function demographics from LinkedIn Ads Reports. |
| [Get Region Demographics](actions/get-region-demographics.md) | GET | Retrieves region demographics from LinkedIn Ads Reports. |
| [Get Seniority Demographics](actions/get-seniority-demographics.md) | GET | Retrieves seniority demographics from LinkedIn Ads Reports. |

