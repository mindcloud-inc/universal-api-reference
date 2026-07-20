# Leadberry: Native API Reference

A consolidated summary of Leadberry's API configuration and 36 documented operations, with links to official documentation.

- **Official docs:** https://www.leadberry.com/integrations
- **API base URL:** `https://app.leadberry.com`

## Authentication

### API Key

Authenticate with the Leadberry API key from Settings > Integrations.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.leadberry.com/pabbly)

## API conventions

Request bodies use URL-encoded form data.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json, text/javascript, */*; q=0.01` |
| `Content-Type` | `application/x-www-form-urlencoded; charset=UTF-8` |

Responses from this API use JSON.

## Pagination

Use `page` in the request body to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `orderBy` in the request body. Set the direction separately with `orderByDir`. Only one sort field is accepted.

## Endpoints (36 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Lead To CRM](actions/add-lead-to-crm.md) | `POST /data/addToCRM` | [docs](https://www.leadberry.com/integrations) |
| [Add Tracking Website](actions/add-tracking-website.md) | `POST /data/addTrackingWebsite` | [docs](https://www.leadberry.com/install-leadberry) |
| [Change Lead Score Level](actions/change-lead-score-level.md) | `POST /data/changeLeadScoreLevel` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Check Tracking Install](actions/check-tracking-install.md) | `POST /data/checkInstall` | [docs](https://www.leadberry.com/install-leadberry) |
| [Check URL Exists](actions/check-url-exists.md) | `POST /data/checkUrlExists` | [docs](https://www.leadberry.com/install-leadberry) |
| [Create Alert Setting](actions/create-alert-setting.md) | `POST /data/saveNewAlertSetting` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Create Lead Note](actions/create-lead-note.md) | `POST /data/saveNewNote` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Disable Website](actions/disable-website.md) | `POST /data/disableSite` | [docs](https://www.leadberry.com/install-leadberry) |
| [Download Email Addresses](actions/download-email-addresses.md) | `POST /data/downloadEmailAddresses` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Estimate Leads For All Website Profile Combinations](actions/estimate-leads-for-all-website-profile-combinations.md) | `GET /data/estimateNumberOfLeadsForAllWidCombinations` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Estimate Number Of Leads](actions/estimate-number-of-leads.md) | `GET /data/estimateNumberOfLeads` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Export Dashboard CSV](actions/export-dashboard-csv.md) | `POST /data/downloadCSVFromDashboard` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Export Leads CSV](actions/export-leads-csv.md) | `POST /data/exportCSV` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Get Crawler Site Results](actions/get-crawler-site-results.md) | `GET /data/getCrawlerSiteResults` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Get CRM Additional Info](actions/get-crm-additional-info.md) | `GET /data/getCRMAdditionalInfo` | [docs](https://www.leadberry.com/integrations) |
| [Get Similar Lead Details](actions/get-similar-lead-details.md) | `GET /data/getLBSimilarDetailsData` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Get User Settings](actions/get-user-settings.md) | `GET /data/getUserSettings` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [List Added Profiles](actions/list-added-profiles.md) | `GET /data/getAddedProfiles` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [List Leads](actions/list-leads.md) | `POST /data/getLeads` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [List Websites](actions/list-websites.md) | `POST /data/getAccounts` | [docs](https://www.leadberry.com/zapier) |
| [Remove Alert Setting](actions/remove-alert-setting.md) | `POST /data/removeAlertSetting` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Remove CRM Connection](actions/remove-crm-connection.md) | `POST /data/removeCRM` | [docs](https://www.leadberry.com/integrations) |
| [Remove Lead Note](actions/remove-lead-note.md) | `POST /data/removeNote` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Remove Pabbly Webhook](actions/remove-pabbly-webhook.md) | `POST /pabbly/remove-webhook` | [docs](https://www.leadberry.com/pabbly) |
| [Request Pabbly API Key](actions/request-pabbly-api-key.md) | `GET /pabbly/requestApiKey` | [docs](https://www.leadberry.com/pabbly) |
| [Request Zapier API Key](actions/request-zapier-api-key.md) | `GET /zapier/requestApiKey` | [docs](https://www.leadberry.com/zapier) |
| [Request Zoho Grant Code](actions/request-zoho-grant-code.md) | `GET /zoho/grant-code` | [docs](https://www.leadberry.com/zoho-crm) |
| [Save Pabbly Webhook](actions/save-pabbly-webhook.md) | `POST /pabbly/save-webhook` | [docs](https://www.leadberry.com/pabbly) |
| [Save Slack View](actions/save-slack-view.md) | `POST /data/saveSlackView` | [docs](https://www.leadberry.com/slack) |
| [Search Profiles](actions/search-profiles.md) | `POST /data/queryProfiles` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Search Similar Companies](actions/search-similar-companies.md) | `POST /data/searchSimilar` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Send Lead Email](actions/send-lead-email.md) | `POST /data/sendLeadEmail` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Test Pabbly Webhook](actions/test-pabbly-webhook.md) | `POST /pabbly/test-webhook` | [docs](https://www.leadberry.com/pabbly) |
| [Update Alert Setting](actions/update-alert-setting.md) | `POST /data/updateAlertSetting` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Update User Settings](actions/update-user-settings.md) | `POST /data/changeUserSettings` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
| [Whitelist Website](actions/whitelist-website.md) | `POST /data/whiteListSite` | [docs](https://app.leadberry.com/js/dist/all.min.js?ver=20221103_1) |
