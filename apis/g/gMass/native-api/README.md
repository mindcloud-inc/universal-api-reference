# GMass: Native API Reference

A consolidated summary of GMass's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api.gmass.co/docs
- **OpenAPI specification:** https://api.gmass.co/swagger/docs/v1
- **API base URL:** `https://api.gmass.co/api`

## Authentication

### API Key

Authenticate GMass requests with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.gmass.co/blog/transactional-emails-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Account Unsubscribe](actions/add-account-unsubscribe.md) | `POST /unsubscribes` | [docs](https://api.gmass.co/docs#tag/Unsubscribes/operation/Unsubscribes_AddUnsubscribe) |
| [Add Campaign Unsubscribe](actions/add-campaign-unsubscribe.md) | `POST /unsubscribes/:campaignId` | [docs](https://api.gmass.co/docs#tag/Unsubscribes/operation/Unsubscribes_AddUnsubscribeForCampaign) |
| [Add Unsubscribed Domain](actions/add-unsubscribed-domain.md) | `POST /unsubscribes/domain/:domain` | [docs](https://api.gmass.co/docs#tag/Unsubscribes/operation/Unsubscribes_AddUnsubscribeDomain) |
| [Create Campaign Draft](actions/create-campaign-draft.md) | `POST /campaigndrafts` | [docs](https://api.gmass.co/docs#tag/CampaignDrafts/operation/CampaignDrafts_Index) |
| [Create Email List](actions/create-email-list.md) | `POST /lists` | [docs](https://api.gmass.co/docs#tag/Lists/operation/Lists_CreateEmailList) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:campaignId` | [docs](https://api.gmass.co/docs#tag/Campaigns/operation/Campaigns_GetCampaign) |
| [Get User](actions/get-user.md) | `GET /user` | [docs](https://api.gmass.co/docs) |
| [Get Warmup Stats](actions/get-warmup-stats.md) | `GET /user/WarmupStats` | [docs](https://api.gmass.co/docs#tag/User/operation/User_WarmupStats) |
| [List Campaign Blocks](actions/list-campaign-blocks.md) | `GET /reports/:campaignId/blocks` | [docs](https://api.gmass.co/docs#tag/Reports/operation/Reports_Blocks) |
| [List Campaign Bounces](actions/list-campaign-bounces.md) | `GET /reports/:campaignId/bounces` | [docs](https://api.gmass.co/docs#tag/Reports/operation/Reports_Bounces) |
| [List Campaign Clicks](actions/list-campaign-clicks.md) | `GET /reports/:campaignId/clicks` | [docs](https://api.gmass.co/docs#tag/Reports/operation/Reports_Clicks) |
| [List Campaign Opens](actions/list-campaign-opens.md) | `GET /reports/:campaignId/opens` | [docs](https://api.gmass.co/docs#tag/Reports/operation/Reports_Opens) |
| [List Campaign Recipients](actions/list-campaign-recipients.md) | `GET /reports/:campaignId/recipients` | [docs](https://api.gmass.co/docs#tag/Reports/operation/Reports_Recipients) |
| [List Campaign Replies](actions/list-campaign-replies.md) | `GET /reports/:campaignId/replies` | [docs](https://api.gmass.co/docs#tag/Reports/operation/Reports_Replies) |
| [List Campaign Unsubscribes](actions/list-campaign-unsubscribes.md) | `GET /reports/:campaignId/unsubscribes` | [docs](https://api.gmass.co/docs#tag/Reports/operation/Reports_Unsubscribes) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://api.gmass.co/docs#tag/Campaigns) |
| [List Campaigns For Zapier](actions/list-campaigns-for-zapier.md) | `GET /campaigns/zapier` | [docs](https://api.gmass.co/docs#tag/Campaigns/operation/Campaigns_Zapier) |
| [List Email Lists](actions/list-email-lists.md) | `GET /lists` | [docs](https://api.gmass.co/docs#tag/Lists/operation/Lists_Lists) |
| [List Google Sheets](actions/list-google-sheets.md) | `GET /sheets` | [docs](https://api.gmass.co/docs#tag/Sheets/operation/Sheets_Index) |
| [List Sample Bounces](actions/list-sample-bounces.md) | `GET /sample/bounces` | [docs](https://api.gmass.co/docs#tag/Sample/operation/Sample_GetSampleBounces) |
| [List Sample Clicks](actions/list-sample-clicks.md) | `GET /sample/clicks` | [docs](https://api.gmass.co/docs#tag/Sample/operation/Sample_GetSampleClicks) |
| [List Sample Opens](actions/list-sample-opens.md) | `GET /sample/opens` | [docs](https://api.gmass.co/docs#tag/Sample/operation/Sample_GetSampleOpens) |
| [List Sample Replies](actions/list-sample-replies.md) | `GET /sample/replies` | [docs](https://api.gmass.co/docs#tag/Sample/operation/Sample_GetSampleReplies) |
| [List Sample Unsubscribes](actions/list-sample-unsubscribes.md) | `GET /sample/unsubscribes` | [docs](https://api.gmass.co/docs#tag/Sample/operation/Sample_GetSampleUnsubscribes) |
| [List Sheet Worksheets](actions/list-sheet-worksheets.md) | `GET /sheets/:sheetid/worksheets` | [docs](https://api.gmass.co/docs#tag/Sheets/operation/Sheets_WorksheetList) |
| [List Unsubscribed Domains](actions/list-unsubscribed-domains.md) | `GET /unsubscribes/domains` | [docs](https://api.gmass.co/docs#tag/Unsubscribes/operation/Unsubscribes_Index) |
| [Remove Account Unsubscribe](actions/remove-account-unsubscribe.md) | `DELETE /unsubscribes` | [docs](https://api.gmass.co/docs#tag/Unsubscribes/operation/Unsubscribes_DeleteUnsubscribe) |
| [Remove Unsubscribed Domain](actions/remove-unsubscribed-domain.md) | `DELETE /unsubscribes/domain/:domain` | [docs](https://api.gmass.co/docs#tag/Unsubscribes/operation/Unsubscribes_DeleteUnsubscribeDomain) |
| [Send Campaign From Draft](actions/send-campaign-from-draft.md) | `POST /campaigns/:campaignDraftId` | [docs](https://api.gmass.co/docs#tag/Campaigns) |
| [Send Transactional Email](actions/send-transactional-email.md) | `POST /transactional` | [docs](https://api.gmass.co/docs#tag/Transactional/operation/Transactional_IndexAsync) |
