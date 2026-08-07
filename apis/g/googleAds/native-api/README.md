# Google Ads: Native API Reference

A consolidated summary of Google Ads's API configuration and 93 documented operations, with links to official documentation.

- **Official docs:** https://developers.google.com/google-ads/api
- **REST base URL:** `https://googleads.googleapis.com/`
- **REST API base URL:** `https://datamanager.googleapis.com`

## Authentication

### OAuth 2.0

OAuth 2.0 authentication for Google Ads API access. Requires a Google Ads developer token and optional manager Login Customer ID for manager-account access.

### Credentials

- **Developer Token:** `googleAdsDeveloperToken` · required · Google Ads developer token from API Center. Required for all Google Ads API requests.
- **Login Customer ID:** `loginCustomerId` · optional · Optional manager account customer ID used as the login-customer-id header when accessing client accounts.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.google.com/o/oauth2/v2/auth to approve access.
2. Exchange the returned authorization code with a POST request to https://oauth2.googleapis.com/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `https://www.googleapis.com/auth/adwords https://www.googleapis.com/auth/datamanager`.

Refresh expired access tokens with a POST request to https://oauth2.googleapis.com/token.

[Official authentication documentation](https://developers.google.com/google-ads/api/docs/oauth/overview)

## API conventions

### REST

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

### REST API

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Retry behavior

- **REST API:** Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (93 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Campaign Criterion](actions/add-campaign-criterion.md) | `POST v22/customers/:customerId/campaignCriteria:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignCriterionService/MutateCampaignCriteria) |
| [Add Keyword Criterion](actions/add-keyword-criterion.md) | `POST v22/customers/:customerId/adGroupCriteria:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupCriterionService/MutateAdGroupCriteria) |
| [Add Lead Feedback](actions/add-lead-feedback.md) | `POST v21/customers/:customerId/localServicesLeads/:leadId:provideLeadFeedback` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v21/LocalServicesLeadService/ProvideLeadFeedback) |
| [Add Negative Campaign Keyword](actions/add-negative-campaign-keyword.md) | `POST v22/customers/:customerId/campaignCriteria:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignCriterionService/MutateCampaignCriteria) |
| [Add Offline User Data Job Operations](actions/add-offline-user-data-job-operations.md) | `POST v22/customers/:customerId/offlineUserDataJobs/:offlineUserDataJobId:addOperations` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/OfflineUserDataJobService/AddOfflineUserDataJobOperations) |
| [Attach Ad Group Ad Label](actions/attach-ad-group-ad-label.md) | `POST v22/customers/:customerId/adGroupAdLabels:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupAdLabelService/MutateAdGroupAdLabels) |
| [Attach Ad Group Label](actions/attach-ad-group-label.md) | `POST v22/customers/:customerId/adGroupLabels:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupLabelService/MutateAdGroupLabels) |
| [Attach Campaign Label](actions/attach-campaign-label.md) | `POST v22/customers/:customerId/campaignLabels:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignLabelService/MutateCampaignLabels) |
| [Attach Keyword Label](actions/attach-keyword-label.md) | `POST v22/customers/:customerId/adGroupCriterionLabels:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupCriterionLabelService/MutateAdGroupCriterionLabels) |
| [Create Ad Group](actions/create-ad-group.md) | `POST v22/customers/:customerId/adGroups:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupService/MutateAdGroups) |
| [Create Campaign](actions/create-campaign.md) | `POST v22/customers/:customerId/campaigns:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignService/MutateCampaigns) |
| [Create Campaign Budget](actions/create-campaign-budget.md) | `POST v22/customers/:customerId/campaignBudgets:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignBudgetService/MutateCampaignBudgets) |
| [Create Customer Client](actions/create-customer-client.md) | `POST v22/customers/:customerId:createCustomerClient` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CustomerService/CreateCustomerClient) |
| [Create Offline User Data Job](actions/create-offline-user-data-job.md) | `POST v22/customers/:customerId/offlineUserDataJobs:create` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/OfflineUserDataJobService/CreateOfflineUserDataJob) |
| [Create Responsive Search Ad](actions/create-responsive-search-ad.md) | `POST v22/customers/:customerId/adGroupAds:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupAdService/MutateAdGroupAds) |
| [Detach Ad Group Ad Label](actions/detach-ad-group-ad-label.md) | `POST v22/customers/:customerId/adGroupAdLabels:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupAdLabelService/MutateAdGroupAdLabels) |
| [Detach Ad Group Label](actions/detach-ad-group-label.md) | `POST v22/customers/:customerId/adGroupLabels:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupLabelService/MutateAdGroupLabels) |
| [Detach Campaign Label](actions/detach-campaign-label.md) | `POST v22/customers/:customerId/campaignLabels:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignLabelService/MutateCampaignLabels) |
| [Detach Keyword Label](actions/detach-keyword-label.md) | `POST v22/customers/:customerId/adGroupCriterionLabels:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupCriterionLabelService/MutateAdGroupCriterionLabels) |
| [Enable Ad Group](actions/enable-ad-group.md) | `POST v22/customers/:customerId/adGroups:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupService/MutateAdGroups) |
| [Enable Ad Group Ad](actions/enable-ad-group-ad.md) | `POST v22/customers/:customerId/adGroupAds:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupAdService/MutateAdGroupAds) |
| [Enable Campaign](actions/enable-campaign.md) | `POST v22/customers/:customerId/campaigns:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignService/MutateCampaigns) |
| [Enable Keyword Criterion](actions/enable-keyword-criterion.md) | `POST v22/customers/:customerId/adGroupCriteria:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupCriterionService/MutateAdGroupCriteria) |
| [Generate Ad Group Themes](actions/generate-ad-group-themes.md) | `POST v22/customers/:customerId:generateAdGroupThemes` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/KeywordPlanIdeaService/GenerateAdGroupThemes) |
| [Generate Keyword Forecast Metrics](actions/generate-keyword-forecast-metrics.md) | `POST v22/customers/:customerId:generateKeywordForecastMetrics` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/KeywordPlanIdeaService/GenerateKeywordForecastMetrics) |
| [Generate Keyword Historical Metrics](actions/generate-keyword-historical-metrics.md) | `POST v22/customers/:customerId:generateKeywordHistoricalMetrics` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/KeywordPlanIdeaService/GenerateKeywordHistoricalMetrics) |
| [Generate Keyword Ideas](actions/generate-keyword-ideas.md) | `POST v22/customers/:customerId:generateKeywordIdeas` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/KeywordPlanIdeaService/GenerateKeywordIdeas) |
| [Generate Recommendations](actions/generate-recommendations.md) | `POST v22/customers/:customerId/recommendations:generate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/RecommendationService/GenerateRecommendations) |
| [Get Ad Group Performance](actions/get-ad-group-performance.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Get Ad Performance](actions/get-ad-performance.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Get Asset Performance Report](actions/get-asset-performance-report.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Get Audience Segment Performance Report](actions/get-audience-segment-performance-report.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Get Budget Pacing Report](actions/get-budget-pacing-report.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Get Campaign Daily Trend Report](actions/get-campaign-daily-trend-report.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Get Conversion Action Performance Report](actions/get-conversion-action-performance-report.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Get Customer Overview](actions/get-customer-overview.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Get Day and Hour Performance Report](actions/get-day-and-hour-performance-report.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Get Device Performance Report](actions/get-device-performance-report.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Get Geo Performance Report](actions/get-geo-performance-report.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Get Keyword Performance](actions/get-keyword-performance.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Get Landing Page Performance Report](actions/get-landing-page-performance-report.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Get Local Services Lead](actions/get-local-services-lead.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Get Recommendation](actions/get-recommendation.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Get User List](actions/get-user-list.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [List Accessible Customers](actions/list-accessible-customers.md) | `GET v22/customers:listAccessibleCustomers` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CustomerService/ListAccessibleCustomers) |
| [List Account Budget Proposals](actions/list-account-budget-proposals.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [List Account Budgets](actions/list-account-budgets.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [List Account Change Events](actions/list-account-change-events.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [List Account Change Status](actions/list-account-change-status.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [List Account Labels](actions/list-account-labels.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [List Billing Setups](actions/list-billing-setups.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [List Customer Client Hierarchy](actions/list-customer-client-hierarchy.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [List Customer Client Links](actions/list-customer-client-links.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [List Customer Label Assignments](actions/list-customer-label-assignments.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [List Customer Manager Links](actions/list-customer-manager-links.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [List Customer User Access](actions/list-customer-user-access.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [List Customer User Access Invitations](actions/list-customer-user-access-invitations.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [List Invoices](actions/list-invoices.md) | `GET v22/customers/:customerId/invoices` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/InvoiceService/ListInvoices) |
| [List Local Services Leads](actions/list-local-services-leads.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [List Recommendations](actions/list-recommendations.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Mutate Ad Group Assets](actions/mutate-ad-group-assets.md) | `POST v22/customers/:customerId/adGroupAssets:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupAssetService/MutateAdGroupAssets) |
| [Mutate Asset Set Assets](actions/mutate-asset-set-assets.md) | `POST v22/customers/:customerId/assetSetAssets:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AssetSetAssetService/MutateAssetSetAssets) |
| [Mutate Asset Sets](actions/mutate-asset-sets.md) | `POST v22/customers/:customerId/assetSets:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AssetSetService/MutateAssetSets) |
| [Mutate Assets](actions/mutate-assets.md) | `POST v22/customers/:customerId/assets:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AssetService/MutateAssets) |
| [Mutate Campaign Asset Sets](actions/mutate-campaign-asset-sets.md) | `POST v22/customers/:customerId/campaignAssetSets:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignAssetSetService/MutateCampaignAssetSets) |
| [Mutate Campaign Assets](actions/mutate-campaign-assets.md) | `POST v22/customers/:customerId/campaignAssets:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignAssetService/MutateCampaignAssets) |
| [Mutate Conversion Actions](actions/mutate-conversion-actions.md) | `POST v22/customers/:customerId/conversionActions:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/ConversionActionService/MutateConversionActions) |
| [Mutate Conversion Custom Variables](actions/mutate-conversion-custom-variables.md) | `POST v22/customers/:customerId/conversionCustomVariables:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/ConversionCustomVariableService/MutateConversionCustomVariables) |
| [Mutate Customer Assets](actions/mutate-customer-assets.md) | `POST v22/customers/:customerId/customerAssets:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CustomerAssetService/MutateCustomerAssets) |
| [Mutate Customer Conversion Goals](actions/mutate-customer-conversion-goals.md) | `POST v22/customers/:customerId/customerConversionGoals:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CustomerConversionGoalService/MutateCustomerConversionGoals) |
| [Mutate Resources](actions/mutate-resources.md) | `POST v22/customers/:customerId/googleAds:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Mutate) |
| [Mutate User Lists](actions/mutate-user-lists.md) | `POST v22/customers/:customerId/userLists:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/UserListService/MutateUserLists) |
| [Pause Ad Group](actions/pause-ad-group.md) | `POST v22/customers/:customerId/adGroups:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupService/MutateAdGroups) |
| [Pause Ad Group Ad](actions/pause-ad-group-ad.md) | `POST v22/customers/:customerId/adGroupAds:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupAdService/MutateAdGroupAds) |
| [Pause Campaign](actions/pause-campaign.md) | `POST v22/customers/:customerId/campaigns:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignService/MutateCampaigns) |
| [Pause Keyword Criterion](actions/pause-keyword-criterion.md) | `POST v22/customers/:customerId/adGroupCriteria:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupCriterionService/MutateAdGroupCriteria) |
| [Remove Ad Group](actions/remove-ad-group.md) | `POST v22/customers/:customerId/adGroups:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupService/MutateAdGroups) |
| [Remove Ad Group Ad](actions/remove-ad-group-ad.md) | `POST v22/customers/:customerId/adGroupAds:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupAdService/MutateAdGroupAds) |
| [Remove Campaign](actions/remove-campaign.md) | `POST v22/customers/:customerId/campaigns:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignService/MutateCampaigns) |
| [Remove Campaign Criterion](actions/remove-campaign-criterion.md) | `POST v22/customers/:customerId/campaignCriteria:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignCriterionService/MutateCampaignCriteria) |
| [Remove Keyword Criterion](actions/remove-keyword-criterion.md) | `POST v22/customers/:customerId/adGroupCriteria:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupCriterionService/MutateAdGroupCriteria) |
| [Run Offline User Data Job](actions/run-offline-user-data-job.md) | `POST v22/customers/:customerId/offlineUserDataJobs/:offlineUserDataJobId:run` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/OfflineUserDataJobService/RunOfflineUserDataJob) |
| [Search Google Ads](actions/search-google-ads.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Search Terms Report](actions/search-terms-report.md) | `POST v22/customers/:customerId/googleAds:search` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/GoogleAdsService/Search) |
| [Update Ad Group](actions/update-ad-group.md) | `POST v22/customers/:customerId/adGroups:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupService/MutateAdGroups) |
| [Update Campaign](actions/update-campaign.md) | `POST v22/customers/:customerId/campaigns:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignService/MutateCampaigns) |
| [Update Campaign Budget](actions/update-campaign-budget.md) | `POST v22/customers/:customerId/campaignBudgets:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignBudgetService/MutateCampaignBudgets) |
| [Update Campaign Criterion](actions/update-campaign-criterion.md) | `POST v22/customers/:customerId/campaignCriteria:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/CampaignCriterionService/MutateCampaignCriteria) |
| [Update Keyword Criterion](actions/update-keyword-criterion.md) | `POST v22/customers/:customerId/adGroupCriteria:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupCriterionService/MutateAdGroupCriteria) |
| [Update Responsive Search Ad](actions/update-responsive-search-ad.md) | `POST v22/customers/:customerId/adGroupAds:mutate` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/AdGroupAdService/MutateAdGroupAds) |
| [Upload Call Conversions](actions/upload-call-conversions.md) | `POST v22/customers/:customerId:uploadCallConversions` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/ConversionUploadService/UploadCallConversions) |
| [Upload Click Conversions](actions/upload-click-conversions.md) | `POST v22/customers/:customerId:uploadClickConversions` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/ConversionUploadService/UploadClickConversions) |
| [Upload Conversion Adjustments](actions/upload-conversion-adjustments.md) | `POST v22/customers/:customerId:uploadConversionAdjustments` | [docs](https://developers.google.com/google-ads/api/reference/rpc/v22/ConversionAdjustmentUploadService/UploadConversionAdjustments) |
