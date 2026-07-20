# ChipBot: Native API Reference

A consolidated summary of ChipBot's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://getchipbot.com/api-docs
- **API base URL:** `https://getchipbot.com`

## Authentication

### Domain API Token

Use a ChipBot domain API token from Settings > Integrations, plus the matching accountId and domainId. The official ChipBot auth docs state this token expires after 1 hour, so it must be refreshed when the Connect test starts failing.

### Credentials

- **API Key:** `apiKey` · required
- **Account ID:** `accountId` · required · Your ChipBot account identifier from the same Integrations screen as the domain token. Example: act_xxx.
- **Domain ID:** `domainId` · required · Your ChipBot domain identifier from the same Integrations screen as the domain token. Example: dom_xxx.

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://getchipbot.com/api-docs/general/domain-auth)

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Connect Domain](actions/connect-domain.md) | `POST /api/v1/connect` | [docs](https://getchipbot.com/api-docs/general/domain-auth) |
| [Delete Video](actions/delete-video.md) | `DELETE /api/v2/connect/accounts/:accountId/domains/:domainId/video-exp/:videoExpId` | [docs](https://getchipbot.com/api-docs/video-exp/delete) |
| [Get Detailed Unique Hits Report](actions/get-detailed-unique-hits-report.md) | `GET /api/v2/connect/accounts/:accountId/domains/:domainId/reporting/analytics/unique-hits/detailed` | [docs](https://getchipbot.com/api-docs/general/unique-hits-report) |
| [Get Detailed Video Analytics](actions/get-detailed-video-analytics.md) | `GET /api/v2/connect/accounts/:accountId/domains/:domainId/video-exp/:videoExpId/reporting/detailed` | [docs](https://getchipbot.com/api-docs/video-exp/video-analytics-detailed) |
| [Get Thread](actions/get-thread.md) | `GET /api/v2/connect/accounts/:accountId/domains/:domainId/kb-tree/:parentId` | [docs](https://getchipbot.com/api-docs/chat-api/get-a-thread) |
| [Get Unique Hits Report](actions/get-unique-hits-report.md) | `GET /api/v2/connect/accounts/:accountId/domains/:domainId/reporting/analytics/unique-hits` | [docs](https://getchipbot.com/api-docs/general/unique-hits-report) |
| [Get Video](actions/get-video.md) | `GET /api/v2/connect/accounts/:accountId/domains/:domainId/video-exp/:videoExpId` | [docs](https://getchipbot.com/api-docs/video-exp/read) |
| [Get Video Analytics Summary](actions/get-video-analytics-summary.md) | `GET /api/v2/connect/accounts/:accountId/domains/:domainId/video-exp/:videoExpId/reporting/summary` | [docs](https://getchipbot.com/api-docs/video-exp/video-analytics-summary) |
| [Get Video Analytics Views by URL](actions/get-video-analytics-views-by-url.md) | `GET /api/v2/connect/accounts/:accountId/domains/:domainId/video-exp/:videoExpId/reporting/views-by-url` | [docs](https://getchipbot.com/api-docs/video-exp/video-analytics-views-by-url) |
| [List Articles](actions/list-articles.md) | `GET /api/v1/connect/accounts/:accountId/domains/:domainId/insights` | [docs](https://getchipbot.com/api-docs/help-desk-api/list) |
| [List Videos](actions/list-videos.md) | `GET /api/v2/connect/accounts/:accountId/domains/:domainId/video-exp` | [docs](https://getchipbot.com/api-docs/video-exp/list) |
| [Reply to Message](actions/reply-to-message.md) | `POST /api/v2/connect/accounts/:accountId/domains/:domainId/messages` | [docs](https://getchipbot.com/api-docs/chat-api/reply-to-a-message) |
| [Request Video Service Token](actions/request-video-service-token.md) | `GET /api/v2/connect/accounts/:accountId/domains/:domainId/videos/tokens` | [docs](https://getchipbot.com/api-docs/video-exp/video-upload) |
| [Request Video Upload Token](actions/request-video-upload-token.md) | `POST /api/v2/utility/video-upload/request` | [docs](https://getchipbot.com/api-docs/video-exp/video-upload) |
