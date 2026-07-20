# LinkedIn Ads Reports: Native API Reference

A consolidated summary of LinkedIn Ads Reports's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads-reporting/ads-reporting?view=li-lms-2026-03
- **API base URL:** `https://api.linkedin.com`

## Authentication

### LinkedIn OAuth2

LinkedIn 3-legged OAuth for Marketing API reporting access.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://www.linkedin.com/oauth/v2/authorization to approve access.
2. Exchange the returned authorization code with a POST request to https://www.linkedin.com/oauth/v2/accessToken.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `r_ads_reporting`.

[Official authentication documentation](https://learn.microsoft.com/en-us/linkedin/shared/authentication/authorization-code-flow?context=linkedin%2Fmarketing%2Fcontext)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `LinkedIn-Version` | `202604` |
| `X-Restli-Protocol-Version` | `2.0.0` |

Responses from this API use JSON. Response data is read from `elements`.

## Pagination

Use `count` in the query string to set the page size (default 100; accepted range 1–1000). Use `start` in the query string as the record offset; numbering starts at 0.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Account Analytics](actions/get-account-analytics.md) | `GET /rest/adAnalytics?q=analytics&pivot=ACCOUNT&dateRange=(start:(year:{{startYear}},month:{{startMonth}},day:{{startDay}}),end:(year:{{endYear}},month:{{endMonth}},day:{{endDay}}))&timeGranularity={{timeGranularity}}&{{facet}}` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads-reporting/ads-reporting?view=li-lms-2026-03) |
| [Get Ad Account](actions/get-ad-account.md) | `GET /rest/adAccounts/{{adAccountId}}` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads/account-structure/create-and-manage-accounts?view=li-lms-2026-01) |
| [Get Ad Analytics](actions/get-ad-analytics.md) | `GET /rest/adAnalytics?q=analytics&pivot={{pivot}}&dateRange=(start:(year:{{startYear}},month:{{startMonth}},day:{{startDay}}),end:(year:{{endYear}},month:{{endMonth}},day:{{endDay}}))&timeGranularity={{timeGranularity}}&{{facet}}` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads-reporting/ads-reporting?view=li-lms-2026-03) |
| [Get Ad Statistics](actions/get-ad-statistics.md) | `GET /rest/adAnalytics?q=statistics&pivots={{pivots}}&dateRange=(start:(year:{{startYear}},month:{{startMonth}},day:{{startDay}}),end:(year:{{endYear}},month:{{endMonth}},day:{{endDay}}))&timeGranularity={{timeGranularity}}&{{facet}}` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads-reporting/ads-reporting?view=li-lms-2026-03) |
| [Get Campaign](actions/get-campaign.md) | `GET /rest/adAccounts/{{adAccountId}}/adCampaigns/{{campaignId}}` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads/account-structure/create-and-manage-campaigns?view=li-lms-2026-04) |
| [Get Campaign Analytics](actions/get-campaign-analytics.md) | `GET /rest/adAnalytics?q=analytics&pivot=CAMPAIGN&dateRange=(start:(year:{{startYear}},month:{{startMonth}},day:{{startDay}}),end:(year:{{endYear}},month:{{endMonth}},day:{{endDay}}))&timeGranularity={{timeGranularity}}&{{facet}}` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads-reporting/ads-reporting?view=li-lms-2026-03) |
| [Get Campaign Group](actions/get-campaign-group.md) | `GET /rest/adAccounts/{{adAccountId}}/adCampaignGroups/{{campaignGroupId}}` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads/account-structure/create-and-manage-campaign-groups?view=li-lms-2026-04) |
| [Get Company Demographics](actions/get-company-demographics.md) | `GET /rest/adAnalytics?q=analytics&pivot=MEMBER_COMPANY&dateRange=(start:(year:{{startYear}},month:{{startMonth}},day:{{startDay}}),end:(year:{{endYear}},month:{{endMonth}},day:{{endDay}}))&timeGranularity={{timeGranularity}}&{{facet}}` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads-reporting/ads-reporting?view=li-lms-2026-03) |
| [Get Country Demographics](actions/get-country-demographics.md) | `GET /rest/adAnalytics?q=analytics&pivot=MEMBER_COUNTRY_V2&dateRange=(start:(year:{{startYear}},month:{{startMonth}},day:{{startDay}}),end:(year:{{endYear}},month:{{endMonth}},day:{{endDay}}))&timeGranularity={{timeGranularity}}&{{facet}}` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads-reporting/ads-reporting?view=li-lms-2026-03) |
| [Get Creative](actions/get-creative.md) | `GET /rest/adAccounts/{{adAccountId}}/creatives/{{creativeId}}` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads/account-structure/create-and-manage-creatives?view=li-lms-2026-04) |
| [Get Creative Analytics](actions/get-creative-analytics.md) | `GET /rest/adAnalytics?q=analytics&pivot=CREATIVE&dateRange=(start:(year:{{startYear}},month:{{startMonth}},day:{{startDay}}),end:(year:{{endYear}},month:{{endMonth}},day:{{endDay}}))&timeGranularity={{timeGranularity}}&{{facet}}` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads-reporting/ads-reporting?view=li-lms-2026-03) |
| [Get Industry Demographics](actions/get-industry-demographics.md) | `GET /rest/adAnalytics?q=analytics&pivot=MEMBER_INDUSTRY&dateRange=(start:(year:{{startYear}},month:{{startMonth}},day:{{startDay}}),end:(year:{{endYear}},month:{{endMonth}},day:{{endDay}}))&timeGranularity={{timeGranularity}}&{{facet}}` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads-reporting/ads-reporting?view=li-lms-2026-03) |
| [Get Job Function Demographics](actions/get-job-function-demographics.md) | `GET /rest/adAnalytics?q=analytics&pivot=MEMBER_JOB_FUNCTION&dateRange=(start:(year:{{startYear}},month:{{startMonth}},day:{{startDay}}),end:(year:{{endYear}},month:{{endMonth}},day:{{endDay}}))&timeGranularity={{timeGranularity}}&{{facet}}` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads-reporting/ads-reporting?view=li-lms-2026-03) |
| [Get Region Demographics](actions/get-region-demographics.md) | `GET /rest/adAnalytics?q=analytics&pivot=MEMBER_REGION_V2&dateRange=(start:(year:{{startYear}},month:{{startMonth}},day:{{startDay}}),end:(year:{{endYear}},month:{{endMonth}},day:{{endDay}}))&timeGranularity={{timeGranularity}}&{{facet}}` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads-reporting/ads-reporting?view=li-lms-2026-03) |
| [Get Seniority Demographics](actions/get-seniority-demographics.md) | `GET /rest/adAnalytics?q=analytics&pivot=MEMBER_SENIORITY&dateRange=(start:(year:{{startYear}},month:{{startMonth}},day:{{startDay}}),end:(year:{{endYear}},month:{{endMonth}},day:{{endDay}}))&timeGranularity={{timeGranularity}}&{{facet}}` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads-reporting/ads-reporting?view=li-lms-2026-03) |
| [Search Ad Accounts](actions/search-ad-accounts.md) | `GET /rest/adAccounts` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads/account-structure/create-and-manage-accounts?view=li-lms-2026-01) |
| [Search Campaign Groups](actions/search-campaign-groups.md) | `GET /rest/adAccounts/{{adAccountId}}/adCampaignGroups` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads/account-structure/create-and-manage-campaign-groups?view=li-lms-2026-04) |
| [Search Campaigns](actions/search-campaigns.md) | `GET /rest/adAccounts/{{adAccountId}}/adCampaigns` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads/account-structure/create-and-manage-campaigns?view=li-lms-2026-04) |
| [Search Creatives](actions/search-creatives.md) | `GET /rest/adAccounts/{{adAccountId}}/creatives` | [docs](https://learn.microsoft.com/en-us/linkedin/marketing/integrations/ads/account-structure/create-and-manage-creatives?view=li-lms-2026-04) |
