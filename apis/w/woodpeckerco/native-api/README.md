# Woodpecker.co: Native API Reference

A consolidated summary of Woodpecker.co's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://developers.woodpecker.co/docs/
- **API base URL:** `https://api.woodpecker.co`

## Authentication

### API Key

Use your Woodpecker API key. MindCloud sends it as the x-api-key header required by Woodpecker.

### Credentials

- **API Key:** `apiKey` · required · Woodpecker API key from Settings -> API Keys.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://developers.woodpecker.co/docs/getting-started/authentication/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `content`. The total page count is read from `pagination_data.total_pages`. The current page number is read from `pagination_data.current_page_number`.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Campaign Step](actions/add-campaign-step.md) | `POST /rest/v2/campaigns/[:campaign_id]/steps` | [docs](https://developers.woodpecker.co/docs/campaigns/POST-add-step/) |
| [Add Mailboxes In Bulk](actions/add-mailboxes-in-bulk.md) | `POST /rest/v2/mailboxes/manual_connection/bulk` | [docs](https://developers.woodpecker.co/docs/mailboxes/post-mailboxes/) |
| [Add Prospects To Campaign](actions/add-prospects-to-campaign.md) | `POST /rest/v1/add_prospects_campaign` | [docs](https://developers.woodpecker.co/docs/prospects/POST-add-prospects-campaign/) |
| [Add Prospects To Database](actions/add-prospects-to-database.md) | `POST /rest/v1/add_prospects_list` | [docs](https://developers.woodpecker.co/docs/prospects/POST-add-prospects-list/) |
| [Create Campaign](actions/create-campaign.md) | `POST /rest/v2/campaigns` | [docs](https://developers.woodpecker.co/docs/campaigns/POST-create-campaign/) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /rest/v2/campaigns/[:campaign_id]` | [docs](https://developers.woodpecker.co/docs/campaigns/DELETE-campaign/) |
| [Delete Prospects](actions/delete-prospects.md) | `DELETE /rest/v1/prospects` | [docs](https://developers.woodpecker.co/docs/prospects/DELETE-prospects/) |
| [Edit Campaign](actions/edit-campaign.md) | `POST /rest/v2/campaigns/[:campaign_id]/make_editable` | [docs](https://developers.woodpecker.co/docs/campaigns/POST-editable-campaign/) |
| [Generate General Statistics Report](actions/generate-general-statistics-report.md) | `POST /rest/v2/reports/campaigns` | [docs](https://developers.woodpecker.co/docs/reports/General-statistics/) |
| [Get Campaign](actions/get-campaign.md) | `GET /rest/v2/campaigns/[:campaign_id]` | [docs](https://developers.woodpecker.co/docs/campaigns/GET-campaign/) |
| [Get Campaign Statistics](actions/get-campaign-statistics.md) | `GET /rest/v1/campaign_list` | [docs](https://developers.woodpecker.co/docs/campaigns/GET-campaign-stats-v1/) |
| [Get Current User](actions/get-current-user.md) | `GET /rest/v1/me` | [docs](https://developers.woodpecker.co/docs/getting-started/authentication/) |
| [Get Inbox Messages](actions/get-inbox-messages.md) | `GET /rest/v2/inbox/messages` | [docs](https://developers.woodpecker.co/docs/inbox/get-inbox-messages/) |
| [Get Mailbox](actions/get-mailbox.md) | `GET /rest/v2/mailboxes/[:id]` | [docs](https://developers.woodpecker.co/docs/mailboxes/get-mailbox/) |
| [Get Manual Tasks](actions/get-manual-tasks.md) | `GET /rest/v2/manual_tasks` | [docs](https://developers.woodpecker.co/docs/manual-tasks/get-manual-tasks/) |
| [Get Prospect Responses](actions/get-prospect-responses.md) | `GET /rest/v2/prospects/[:prospect_id]/responses` | [docs](https://developers.woodpecker.co/docs/prospects/GET-prospect-responses/) |
| [List Campaign Prospects](actions/list-campaign-prospects.md) | `GET /rest/v1/prospects` | [docs](https://developers.woodpecker.co/docs/prospects/get-prospects-campaign/) |
| [List Campaigns](actions/list-campaigns.md) | `GET /rest/v1/campaign_list` | [docs](https://developers.woodpecker.co/docs/campaigns/GET-campaign-list-v1/) |
| [List Mailboxes](actions/list-mailboxes.md) | `GET /rest/v2/mailboxes` | [docs](https://developers.woodpecker.co/docs/mailboxes/get-mailboxes/) |
| [List Prospects](actions/list-prospects.md) | `GET /rest/v1/prospects` | [docs](https://developers.woodpecker.co/docs/prospects/get-prospects/) |
| [Pause Campaign](actions/pause-campaign.md) | `POST /rest/v2/campaigns/[:campaign_id]/pause` | [docs](https://developers.woodpecker.co/docs/campaigns/POST-pause-campaign/) |
| [Reply To Message](actions/reply-to-message.md) | `POST /rest/v2/inbox/messages/[:id]/reply` | [docs](https://developers.woodpecker.co/docs/inbox/post-reply-message/) |
| [Run Campaign](actions/run-campaign.md) | `POST /rest/v2/campaigns/[:campaign_id]/run` | [docs](https://developers.woodpecker.co/docs/campaigns/POST-run-campaign/) |
| [Search Prospects](actions/search-prospects.md) | `GET /rest/v1/prospects` | [docs](https://developers.woodpecker.co/docs/prospects/get-search-prospects/) |
| [Stop Campaign](actions/stop-campaign.md) | `POST /rest/v2/campaigns/[:campaign_id]/stop` | [docs](https://developers.woodpecker.co/docs/campaigns/POST-stop-campaign/) |
| [Update Campaign Settings](actions/update-campaign-settings.md) | `PATCH /rest/v2/campaigns/[:campaign_id]` | [docs](https://developers.woodpecker.co/docs/campaigns/PATCH-campaign/) |
| [Update Campaign Step](actions/update-campaign-step.md) | `PATCH /rest/v2/campaigns/[:campaign_id]/steps/[:step_id]` | [docs](https://developers.woodpecker.co/docs/campaigns/PATCH-campaign-step/) |
| [Update Mailbox](actions/update-mailbox.md) | `PATCH /rest/v2/mailboxes/[:smtp_mailbox_id]` | [docs](https://developers.woodpecker.co/docs/mailboxes/update-mailbox/) |
| [Update Prospects In Campaign](actions/update-prospects-in-campaign.md) | `POST /rest/v1/add_prospects_campaign` | [docs](https://developers.woodpecker.co/docs/prospects/POST-update-prospects-campaign/) |
| [Update Prospects In Database](actions/update-prospects-in-database.md) | `POST /rest/v1/add_prospects_list` | [docs](https://developers.woodpecker.co/docs/prospects/POST-update-prospect-list/) |
