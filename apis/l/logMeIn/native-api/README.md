# LogMeIn: Native API Reference

A consolidated summary of LogMeIn's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.goto.com/LogMeInResolve/
- **OpenAPI specification:** https://developer.goto.com/page-data/LogMeInResolve/page-data.json
- **API base URL:** `https://api.goto.com`

## Authentication

### OAuth 2.0

Connect with a GoTo OAuth client that has LogMeIn Resolve access enabled.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://authentication.logmeininc.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://authentication.logmeininc.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `support:`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://authentication.logmeininc.com/oauth/token.

[Official authentication documentation](https://developer.goto.com/guides/Authentication/03_HOW_accessToken/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Acknowledge Alerts](actions/acknowledge-alerts.md) | `POST /goto-resolve-alerts/v1/acknowledge` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Add Incident Comment](actions/add-incident-comment.md) | `POST /goto-resolve-ticketing/v1/incidents/:referenceNum/comments` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Close Session](actions/close-session.md) | `POST /goto-resolve/v1/sessions/:sessionId/close` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Create Document](actions/create-document.md) | `POST /resolve/knowledge-base/v2/documents` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Create Draft Document](actions/create-draft-document.md) | `POST /resolve/knowledge-base/v2/drafts` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Create Folder](actions/create-folder.md) | `POST /resolve/knowledge-base/v2/folders` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Create Incident](actions/create-incident.md) | `POST /goto-resolve-ticketing/v1/incidents` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Create Support Session](actions/create-support-session.md) | `POST /goto-resolve/v1/sessions` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Download Document](actions/download-document.md) | `GET /resolve/knowledge-base/v2/documents/:documentId/download` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Download Draft Document](actions/download-draft-document.md) | `GET /resolve/knowledge-base/v2/drafts/:draftId/download` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Execute Devices GraphQL Query](actions/execute-devices-graphql-query.md) | `POST /goto-resolve-devices/v1` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Execute Reporting GraphQL Query](actions/execute-reporting-graphql-query.md) | `POST /goto-resolve-reporting/v1` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Find Related Documents](actions/find-related-documents.md) | `GET /resolve/knowledge-base/v2/documents/:documentId/related` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Find Related Documents By Text](actions/find-related-documents-by-text.md) | `POST /resolve/knowledge-base/v2/documents/related` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Get Document](actions/get-document.md) | `GET /resolve/knowledge-base/v2/documents/:documentId` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Get Draft Document](actions/get-draft-document.md) | `GET /resolve/knowledge-base/v2/drafts/:draftId` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Get Incident](actions/get-incident.md) | `GET /goto-resolve-ticketing/v1/incidents/:referenceNum` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Get Latest Document Draft](actions/get-latest-document-draft.md) | `GET /resolve/knowledge-base/v2/documents/:documentId/draft` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Get Session Mailto Link](actions/get-session-mailto-link.md) | `GET /goto-resolve/v1/sessions/:sessionId/invite/email` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Get Session State](actions/get-session-state.md) | `GET /goto-resolve/v1/sessions/:sessionId` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Get Ticketing Service](actions/get-ticketing-service.md) | `GET /goto-resolve-ticketing/v1/services/:id` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Get Ticketing Services](actions/get-ticketing-services.md) | `GET /goto-resolve-ticketing/v1/services` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Get User Settings](actions/get-user-settings.md) | `GET /resolve/knowledge-base/v2/user-settings` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [List Alert Subscriptions](actions/list-alert-subscriptions.md) | `GET /goto-resolve-alerts/v1/subscriptions` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [List Alerts](actions/list-alerts.md) | `POST /goto-resolve-alerts/v1/alerts/list` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [List Documents](actions/list-documents.md) | `GET /resolve/knowledge-base/v2/documents` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [List Draft Documents](actions/list-draft-documents.md) | `GET /resolve/knowledge-base/v2/drafts` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [List Folders](actions/list-folders.md) | `GET /resolve/knowledge-base/v2/folders` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [List Incidents](actions/list-incidents.md) | `GET /goto-resolve-ticketing/v1/incidents` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [List Tenants](actions/list-tenants.md) | `GET /goto-resolve-tenants/v1/tenants` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [List Ticketing Users](actions/list-ticketing-users.md) | `GET /goto-resolve-ticketing/v1/users` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Move Document](actions/move-document.md) | `POST /resolve/knowledge-base/v2/documents/:documentId/move` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Publish Draft Document](actions/publish-draft-document.md) | `POST /resolve/knowledge-base/v2/drafts/:draftId/publish` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Send Session SMS Invitation](actions/send-session-sms-invitation.md) | `POST /goto-resolve/v1/sessions/:sessionId/invite/sms` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Update Document](actions/update-document.md) | `PATCH /resolve/knowledge-base/v2/documents/:documentId` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Update Draft Document](actions/update-draft-document.md) | `PATCH /resolve/knowledge-base/v2/drafts/:draftId` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Update Folder](actions/update-folder.md) | `PATCH /resolve/knowledge-base/v2/folders/:folderId` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Update Incident](actions/update-incident.md) | `PUT /goto-resolve-ticketing/v1/incidents/:referenceNum` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Update Incident Comment](actions/update-incident-comment.md) | `PUT /goto-resolve-ticketing/v1/incidents/:referenceNum/comments/:commentId` | [docs](https://developer.goto.com/LogMeInResolve/) |
| [Upsert Alert Webhook Subscription](actions/upsert-alert-webhook-subscription.md) | `PUT /goto-resolve-alerts/v1/subscriptions/:subscriptionId` | [docs](https://developer.goto.com/LogMeInResolve/) |
