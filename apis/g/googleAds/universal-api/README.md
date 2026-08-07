# <img src="https://images.mindcloud.co/apps/icons/google-ads-icon_1782393619275.png" alt="Google Ads logo" width="28" height="28"> Google Ads: Universal API

Create campaigns, measure performance, and optimize Google ad spend.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleAds/latest
- **Category:** Marketing
- **Actions:** 93
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://ads.google.com/
- **Vendor API docs:** https://developers.google.com/google-ads/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Accessible Customers](actions/list-accessible-customers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleAds/latest/actions/list-accessible-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (93)

### Accounts

| Action | Method | Description |
| --- | --- | --- |
| [List Account Budget Proposals](actions/list-account-budget-proposals.md) | GET | Retrieves account budget proposals from Google Ads. |
| [List Account Budgets](actions/list-account-budgets.md) | GET | Retrieves account budgets from Google Ads. |
| [List Billing Setups](actions/list-billing-setups.md) | GET | Retrieves billing setups from Google Ads. |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Add Campaign Criterion](actions/add-campaign-criterion.md) | POST | Creates a campaign criterion in Google Ads. |
| [Add Keyword Criterion](actions/add-keyword-criterion.md) | POST | Creates a keyword criterion in Google Ads. |
| [Add Negative Campaign Keyword](actions/add-negative-campaign-keyword.md) | POST | Creates a negative campaign keyword in Google Ads. |
| [Attach Ad Group Ad Label](actions/attach-ad-group-ad-label.md) | POST | Attaches a label to an ad group ad in Google Ads. |
| [Attach Ad Group Label](actions/attach-ad-group-label.md) | POST | Attaches a label to an ad group in Google Ads. |
| [Attach Campaign Label](actions/attach-campaign-label.md) | POST | Attaches a label to a campaign in Google Ads. |
| [Attach Keyword Label](actions/attach-keyword-label.md) | POST | Attaches a label to a keyword criterion in Google Ads. |
| [Create Ad Group](actions/create-ad-group.md) | POST | Creates an ad group in Google Ads. |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a campaign in Google Ads. |
| [Create Campaign Budget](actions/create-campaign-budget.md) | POST | Creates a campaign budget in Google Ads. |
| [Create Responsive Search Ad](actions/create-responsive-search-ad.md) | POST | Creates a responsive search ad in Google Ads. |
| [Detach Ad Group Ad Label](actions/detach-ad-group-ad-label.md) | DELETE | Detaches a label from an ad group ad in Google Ads. |
| [Detach Ad Group Label](actions/detach-ad-group-label.md) | DELETE | Detaches a label from an ad group in Google Ads. |
| [Detach Campaign Label](actions/detach-campaign-label.md) | DELETE | Detaches a label from a campaign in Google Ads. |
| [Detach Keyword Label](actions/detach-keyword-label.md) | DELETE | Detaches a label from a keyword criterion in Google Ads. |
| [Enable Ad Group](actions/enable-ad-group.md) | PUT | Updates an ad group to enabled status in Google Ads. |
| [Enable Ad Group Ad](actions/enable-ad-group-ad.md) | PUT | Updates an ad group ad to enabled status in Google Ads. |
| [Enable Campaign](actions/enable-campaign.md) | PUT | Updates a campaign to enabled status in Google Ads. |
| [Enable Keyword Criterion](actions/enable-keyword-criterion.md) | PUT | Updates a keyword criterion to enabled status in Google Ads. |
| [Mutate Ad Group Assets](actions/mutate-ad-group-assets.md) | PUT | Creates, updates, or removes ad group assets in Google Ads. |
| [Mutate Asset Set Assets](actions/mutate-asset-set-assets.md) | PUT | Creates, updates, or removes asset set assets in Google Ads. |
| [Mutate Asset Sets](actions/mutate-asset-sets.md) | PUT | Creates, updates, or removes asset sets in Google Ads. |
| [Mutate Assets](actions/mutate-assets.md) | PUT | Creates, updates, or removes assets in Google Ads. |
| [Mutate Campaign Asset Sets](actions/mutate-campaign-asset-sets.md) | PUT | Creates, updates, or removes campaign asset sets in Google Ads. |
| [Mutate Campaign Assets](actions/mutate-campaign-assets.md) | PUT | Creates, updates, or removes campaign assets in Google Ads. |
| [Mutate Conversion Actions](actions/mutate-conversion-actions.md) | PUT | Creates, updates, or removes conversion actions in Google Ads. |
| [Mutate Conversion Custom Variables](actions/mutate-conversion-custom-variables.md) | PUT | Creates, updates, or removes conversion custom variables in Google Ads. |
| [Mutate Customer Assets](actions/mutate-customer-assets.md) | PUT | Creates, updates, or removes customer assets in Google Ads. |
| [Mutate Customer Conversion Goals](actions/mutate-customer-conversion-goals.md) | PUT | Creates, updates, or removes customer conversion goals in Google Ads. |
| [Pause Ad Group](actions/pause-ad-group.md) | PUT | Updates an ad group to paused status in Google Ads. |
| [Pause Ad Group Ad](actions/pause-ad-group-ad.md) | PUT | Updates an ad group ad to paused status in Google Ads. |
| [Pause Campaign](actions/pause-campaign.md) | PUT | Updates a campaign to paused status in Google Ads. |
| [Pause Keyword Criterion](actions/pause-keyword-criterion.md) | PUT | Updates a keyword criterion to paused status in Google Ads. |
| [Remove Ad Group](actions/remove-ad-group.md) | DELETE | Deletes an ad group from Google Ads. |
| [Remove Ad Group Ad](actions/remove-ad-group-ad.md) | DELETE | Deletes an ad group ad from Google Ads. |
| [Remove Campaign](actions/remove-campaign.md) | DELETE | Deletes a campaign from Google Ads. |
| [Remove Campaign Criterion](actions/remove-campaign-criterion.md) | DELETE | Deletes a campaign criterion from Google Ads. |
| [Remove Keyword Criterion](actions/remove-keyword-criterion.md) | DELETE | Deletes a keyword criterion from Google Ads. |
| [Update Ad Group](actions/update-ad-group.md) | PUT | Updates an existing ad group in Google Ads. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in Google Ads. |
| [Update Campaign Budget](actions/update-campaign-budget.md) | PUT | Updates an existing campaign budget in Google Ads. |
| [Update Campaign Criterion](actions/update-campaign-criterion.md) | PUT | Updates an existing campaign criterion in Google Ads. |
| [Update Keyword Criterion](actions/update-keyword-criterion.md) | PUT | Updates an existing keyword criterion in Google Ads. |
| [Update Responsive Search Ad](actions/update-responsive-search-ad.md) | PUT | Updates an existing responsive search ad in Google Ads. |
| [Upload Call Conversions](actions/upload-call-conversions.md) | POST | Uploads call conversions to Google Ads. |
| [Upload Click Conversions](actions/upload-click-conversions.md) | POST | Uploads click conversions to Google Ads. |
| [Upload Conversion Adjustments](actions/upload-conversion-adjustments.md) | PUT | Uploads conversion adjustments to Google Ads. |

### Customers

| Action | Method | Description |
| --- | --- | --- |
| [Create Customer Client](actions/create-customer-client.md) | POST | Creates a customer client in Google Ads. |
| [Get Customer Overview](actions/get-customer-overview.md) | GET |  |
| [List Accessible Customers](actions/list-accessible-customers.md) | GET |  |
| [List Account Labels](actions/list-account-labels.md) | GET | Retrieves account labels from Google Ads. |
| [List Customer Client Hierarchy](actions/list-customer-client-hierarchy.md) | GET | Retrieves customer client hierarchy from Google Ads. |
| [List Customer Client Links](actions/list-customer-client-links.md) | GET | Retrieves customer client links from Google Ads. |
| [List Customer Label Assignments](actions/list-customer-label-assignments.md) | GET | Retrieves customer label assignments from Google Ads. |
| [List Customer Manager Links](actions/list-customer-manager-links.md) | GET | Retrieves customer manager links from Google Ads. |
| [List Customer User Access](actions/list-customer-user-access.md) | GET | Retrieves customer user access from Google Ads. |
| [List Customer User Access Invitations](actions/list-customer-user-access-invitations.md) | GET | Retrieves customer user access invitations from Google Ads. |

### Invoices

| Action | Method | Description |
| --- | --- | --- |
| [List Invoices](actions/list-invoices.md) | GET | Retrieves invoices from your Google Ads account. |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Add Lead Feedback](actions/add-lead-feedback.md) | POST |  |
| [Get Local Services Lead](actions/get-local-services-lead.md) | GET | Retrieves a local services lead from Google Ads. |
| [List Local Services Leads](actions/list-local-services-leads.md) | GET | Retrieves local services leads from Google Ads. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Add Offline User Data Job Operations](actions/add-offline-user-data-job-operations.md) | PUT | Adds operations to an offline user data job in Google Ads. |
| [Create Offline User Data Job](actions/create-offline-user-data-job.md) | POST | Creates an offline user data job in Google Ads. |
| [Get User List](actions/get-user-list.md) | GET | Retrieves a user list from Google Ads. |
| [Mutate User Lists](actions/mutate-user-lists.md) | PUT | Creates, updates, or removes user lists in Google Ads. |
| [Run Offline User Data Job](actions/run-offline-user-data-job.md) | PUT | Runs an offline user data job in Google Ads. |

### Mutate

| Action | Method | Description |
| --- | --- | --- |
| [Mutate Resources](actions/mutate-resources.md) | PUT | Creates, updates, or removes resources in Google Ads. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Generate Ad Group Themes](actions/generate-ad-group-themes.md) | GET | Generates ad group themes in Google Ads. |
| [Generate Keyword Forecast Metrics](actions/generate-keyword-forecast-metrics.md) | GET | Generates keyword forecast metrics in Google Ads. |
| [Generate Keyword Historical Metrics](actions/generate-keyword-historical-metrics.md) | GET | Generates keyword historical metrics in Google Ads. |
| [Generate Keyword Ideas](actions/generate-keyword-ideas.md) | GET | Generates keyword ideas in Google Ads. |
| [Generate Recommendations](actions/generate-recommendations.md) | GET | Generates recommendations for your Google Ads account. |
| [Get Ad Group Performance](actions/get-ad-group-performance.md) | GET |  |
| [Get Ad Performance](actions/get-ad-performance.md) | GET |  |
| [Get Asset Performance Report](actions/get-asset-performance-report.md) | GET | Retrieves an asset performance report from Google Ads. |
| [Get Audience Segment Performance Report](actions/get-audience-segment-performance-report.md) | GET | Retrieves an audience segment performance report from Google Ads. |
| [Get Budget Pacing Report](actions/get-budget-pacing-report.md) | GET | Retrieves a budget pacing report from Google Ads. |
| [Get Campaign Daily Trend Report](actions/get-campaign-daily-trend-report.md) | GET | Retrieves a campaign daily trend report from Google Ads. |
| [Get Conversion Action Performance Report](actions/get-conversion-action-performance-report.md) | GET | Retrieves a conversion action performance report from Google Ads. |
| [Get Day and Hour Performance Report](actions/get-day-and-hour-performance-report.md) | GET | Retrieves a day and hour performance report from Google Ads. |
| [Get Device Performance Report](actions/get-device-performance-report.md) | GET | Retrieves a device performance report from Google Ads. |
| [Get Geo Performance Report](actions/get-geo-performance-report.md) | GET | Retrieves a geo performance report from Google Ads. |
| [Get Keyword Performance](actions/get-keyword-performance.md) | GET |  |
| [Get Landing Page Performance Report](actions/get-landing-page-performance-report.md) | GET | Retrieves a landing page performance report from Google Ads. |
| [Get Recommendation](actions/get-recommendation.md) | GET | Retrieves a recommendation from Google Ads. |
| [List Account Change Events](actions/list-account-change-events.md) | GET | Retrieves account change events from Google Ads. |
| [List Account Change Status](actions/list-account-change-status.md) | GET | Retrieves account change status from Google Ads. |
| [List Recommendations](actions/list-recommendations.md) | GET | Retrieves recommendations from your Google Ads account. |
| [Search Google Ads](actions/search-google-ads.md) | GET | Searches Google Ads using a custom GAQL query. |
| [Search Terms Report](actions/search-terms-report.md) | GET | Retrieves a search terms report from Google Ads. |

