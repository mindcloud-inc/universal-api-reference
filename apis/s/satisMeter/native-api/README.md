# SatisMeter: Native API Reference

A consolidated summary of SatisMeter's API configuration and 13 documented operations, with links to official documentation.

- **Official docs:** https://app.satismeter.com/apidoc
- **API base URL:** `https://app.satismeter.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://app.satismeter.com/apidoc)

## API conventions

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `page.nextPageCursor`.

## Pagination

Use `pageSize` in the query string to set the page size (default 20; accepted range 1–100). Use `pageCursor` in the query string as the pagination cursor.

## Endpoints (13 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Delete User](actions/delete-user.md) | `DELETE /api/users/:userId` | [docs](https://support.satismeter.com/hc/en-us/articles/6980450524179-Delete-user-API) |
| [Get Project](actions/get-project.md) | `GET /api/v3/projects/:projectId` | [docs](https://app.satismeter.com/apidoc#tag/Project/paths/~1projects~1{projectId}/get) |
| [Get Survey](actions/get-survey.md) | `GET /api/v3/projects/:projectId/campaigns/:campaignId` | [docs](https://app.satismeter.com/apidoc#tag/Surveys/paths/~1projects~1{projectId}~1campaigns~1{campaignId}/get) |
| [Get Survey Statistics](actions/get-survey-statistics.md) | `GET /api/v3/projects/:projectId/campaigns/:campaignId/statistics` | [docs](https://app.satismeter.com/apidoc#tag/Statistics/paths/~1projects~1{projectId}~1campaigns~1{campaignId}~1statistics/get) |
| [Insert NPS Survey Response](actions/insert-nps-survey-response.md) | `POST /api/responses` | [docs](https://support.satismeter.com/hc/en-us/articles/6980464243475-Insert-response-API) |
| [List Project Responses](actions/list-project-responses.md) | `GET /api/v3/projects/:projectId/responses` | [docs](https://app.satismeter.com/apidoc#tag/Responses/paths/~1projects~1{projectId}~1responses/get) |
| [List Survey Responses](actions/list-survey-responses.md) | `GET /api/v3/projects/:projectId/campaigns/:campaignId/responses` | [docs](https://app.satismeter.com/apidoc#tag/Responses/paths/~1projects~1{projectId}~1campaigns~1{campaignId}~1responses/get) |
| [List Surveys](actions/list-surveys.md) | `GET /api/v3/projects/:projectId/campaigns` | [docs](https://app.satismeter.com/apidoc#tag/Surveys/paths/~1projects~1{projectId}~1campaigns/get) |
| [List Unsubscribed Emails](actions/list-unsubscribed-emails.md) | `GET /api/v2/project-unsubscribes/:projectId` | [docs](https://support.satismeter.com/hc/en-us/articles/6980458958995-Unsubscribe-email-API) |
| [List Users](actions/list-users.md) | `GET /api/users` | [docs](https://support.satismeter.com/hc/en-us/articles/6980473872531-List-users-API) |
| [Track Event](actions/track-event.md) | `POST /api/users` | [docs](https://support.satismeter.com/hc/en-us/articles/6980481518227-Track-event-API) |
| [Update Unsubscribed Emails](actions/update-unsubscribed-emails.md) | `PATCH /api/v2/project-unsubscribes/:projectId` | [docs](https://support.satismeter.com/hc/en-us/articles/6980458958995-Unsubscribe-email-API) |
| [Upsert User](actions/upsert-user.md) | `POST /api/users` | [docs](https://support.satismeter.com/hc/en-us/articles/6980457910163-Insert-Update-user-API) |
