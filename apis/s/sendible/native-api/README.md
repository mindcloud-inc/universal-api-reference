# Sendible: Native API Reference

A consolidated summary of Sendible's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://support.sendible.com/hc/en-us
- **API base URL:** `https://api.sendible.com`

## Authentication

### API Key

Authenticate Sendible API requests with an access token sent as a query parameter.

### Credentials

- **API Key:** `apiKey` · required
- **User ID:** `userId` · optional · Sendible numeric user or dashboard ID used by some endpoints.
- **Email:** `email` · optional · Sendible account email used by calendar endpoints.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://support.sendible.com/hc/en-us)

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Abort Upload](actions/abort-upload.md) | `DELETE 0.2/tw/uploads` | [docs](https://support.sendible.com/hc/en-us) |
| [Complete Upload](actions/complete-upload.md) | `PUT 0.2/tw/uploads` | [docs](https://support.sendible.com/hc/en-us) |
| [Create Media](actions/create-media.md) | `POST 0.2/tw/media` | [docs](https://support.sendible.com/hc/en-us) |
| [Create Media Library](actions/create-media-library.md) | `POST 0.1/tw/media_libraries` | [docs](https://support.sendible.com/hc/en-us) |
| [Create Upload Intent](actions/create-upload-intent.md) | `POST 0.2/tw/uploads` | [docs](https://support.sendible.com/hc/en-us) |
| [Delete Media](actions/delete-media.md) | `DELETE 0.2/tw/media` | [docs](https://support.sendible.com/hc/en-us) |
| [Delete Media Library](actions/delete-media-library.md) | `DELETE 0.1/tw/media_libraries` | [docs](https://support.sendible.com/hc/en-us) |
| [Disable Feature Tag](actions/disable-feature-tag.md) | `DELETE api/v2/features` | [docs](https://support.sendible.com/hc/en-us) |
| [Enable Feature Tag](actions/enable-feature-tag.md) | `POST api/v2/features` | [docs](https://support.sendible.com/hc/en-us) |
| [Generate AI Content Variation](actions/generate-ai-content-variation.md) | `GET 1.0/api/ai/content` | [docs](https://support.sendible.com/hc/en-us) |
| [Generate AI Text](actions/generate-ai-text.md) | `GET 1.0/api/ai/text_generation` | [docs](https://support.sendible.com/hc/en-us) |
| [Get Account](actions/get-account.md) | `GET api/v3/account` | [docs](https://support.sendible.com/hc/en-us) |
| [Get Calendar Message](actions/get-calendar-message.md) | `GET https://api.prd-tw.sendible.com/v1.0/messages/{{messageId}}` | [docs](https://support.sendible.com/hc/en-us) |
| [Get Campaign](actions/get-campaign.md) | `GET 1.0/api/campaign` | [docs](https://support.sendible.com/hc/en-us) |
| [Get Campaign Audience Report](actions/get-campaign-audience-report.md) | `GET 1.0/api/campaign/report/audience` | [docs](https://support.sendible.com/hc/en-us) |
| [Get Campaign Overview](actions/get-campaign-overview.md) | `GET 1.0/api/campaign/overview` | [docs](https://support.sendible.com/hc/en-us) |
| [Get Campaign Overview Report](actions/get-campaign-overview-report.md) | `GET 1.0/api/campaign/report/overview` | [docs](https://support.sendible.com/hc/en-us) |
| [Get Campaign Posts Report](actions/get-campaign-posts-report.md) | `GET 1.0/api/campaign/report/posts` | [docs](https://support.sendible.com/hc/en-us) |
| [Get Link Preview](actions/get-link-preview.md) | `GET api/v0/linkpreview.json` | [docs](https://support.sendible.com/hc/en-us) |
| [Get Media](actions/get-media.md) | `GET 0.2/tw/media` | [docs](https://support.sendible.com/hc/en-us) |
| [Get TikTok Report](actions/get-tik-tok-report.md) | `GET 0.2/tw/tiktok/report` | [docs](https://support.sendible.com/hc/en-us) |
| [List Accounts](actions/list-accounts.md) | `GET api/v2/accounts.json` | [docs](https://support.sendible.com/hc/en-us) |
| [List Calendar Messages](actions/list-calendar-messages.md) | `GET 0.1/tw/messages` | [docs](https://support.sendible.com/hc/en-us) |
| [List Calendar Summary](actions/list-calendar-summary.md) | `GET 0.1/tw/messages/summary` | [docs](https://support.sendible.com/hc/en-us) |
| [List Campaigns](actions/list-campaigns.md) | `GET 1.0/api/campaigns` | [docs](https://support.sendible.com/hc/en-us) |
| [List Filters](actions/list-filters.md) | `GET 0.1/tw/filters` | [docs](https://support.sendible.com/hc/en-us) |
| [List Holidays](actions/list-holidays.md) | `GET https://api.prd-tw.sendible.com/v1.0/holidays` | [docs](https://support.sendible.com/hc/en-us) |
| [List Media](actions/list-media.md) | `GET 0.2/tw/media` | [docs](https://support.sendible.com/hc/en-us) |
| [List Media Libraries](actions/list-media-libraries.md) | `GET 0.1/tw/media_libraries` | [docs](https://support.sendible.com/hc/en-us) |
| [List Queues](actions/list-queues.md) | `GET 1.0/api/queues` | [docs](https://support.sendible.com/hc/en-us) |
| [List Quick Reports](actions/list-quick-reports.md) | `GET api/v2/quick_reports.json` | [docs](https://support.sendible.com/hc/en-us) |
| [List Recent Media](actions/list-recent-media.md) | `GET api/v2/media.json` | [docs](https://support.sendible.com/hc/en-us) |
| [List Reminders](actions/list-reminders.md) | `GET 1.0/tw/reminders` | [docs](https://support.sendible.com/hc/en-us) |
| [List Togglable Features](actions/list-togglable-features.md) | `GET https://api.prd-tw.sendible.com/v1.0/features/toggles` | [docs](https://support.sendible.com/hc/en-us) |
| [List Users](actions/list-users.md) | `GET api/v0/users.json` | [docs](https://support.sendible.com/hc/en-us) |
| [Rename Media](actions/rename-media.md) | `PUT 0.2/tw/media` | [docs](https://support.sendible.com/hc/en-us) |
| [Rename Media Library](actions/rename-media-library.md) | `PUT 0.1/tw/media_libraries` | [docs](https://support.sendible.com/hc/en-us) |
| [Reschedule Message](actions/reschedule-message.md) | `POST 0.1/tw/messages/reschedule` | [docs](https://support.sendible.com/hc/en-us) |
| [Resolve Message Recipients](actions/resolve-message-recipients.md) | `POST https://api.prd-tw.sendible.com/v1.0/messages/{{messageId}}/resolve` | [docs](https://support.sendible.com/hc/en-us) |
| [Search Images](actions/search-images.md) | `GET api/v3/images/search/{{integration}}.json` | [docs](https://support.sendible.com/hc/en-us) |
