# Hireflix: Native API Reference

A consolidated summary of Hireflix's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://api.hireflix.com/
- **API base URL:** `https://api.hireflix.com`

## Authentication

### API Key

Connect with a Hireflix API key generated from your Hireflix account.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.hireflix.com/article/c6l3n1qgrw-integrating-hireflix-in-your-ats)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Interview Comment](actions/add-interview-comment.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Archive Interview](actions/archive-interview.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Create Interview Share Link](actions/create-interview-share-link.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Create Webhook](actions/create-webhook.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Get Current User Info](actions/get-current-user-info.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Get Interview](actions/get-interview.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Get Interview Candidate](actions/get-interview-candidate.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Get Interview Scores](actions/get-interview-scores.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Get Interview Thumbnails](actions/get-interview-thumbnails.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Get Interview Tracking](actions/get-interview-tracking.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Get Interview User Metadata](actions/get-interview-user-metadata.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Get Permissions](actions/get-permissions.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Get Position](actions/get-position.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Get Position Interview Stats](actions/get-position-interview-stats.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Get Position Public Submission Settings](actions/get-position-public-submission-settings.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Get Template](actions/get-template.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Get Theme](actions/get-theme.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Get Usage](actions/get-usage.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Get Webhook](actions/get-webhook.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Get Webhook Secret Key](actions/get-webhook-secret-key.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Invite Candidate To Interview](actions/invite-candidate-to-interview.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [List API Keys](actions/list-api-keys.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [List Interview Comments](actions/list-interview-comments.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [List Interview Steps](actions/list-interview-steps.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [List Position Interviews](actions/list-position-interviews.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [List Position Questions](actions/list-position-questions.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [List Position Shareable Links](actions/list-position-shareable-links.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [List Position Tags](actions/list-position-tags.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [List Position Users](actions/list-position-users.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [List Positions](actions/list-positions.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [List Tags for Position](actions/list-tags-for-position.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [List Templates](actions/list-templates.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [List Themes](actions/list-themes.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [List Webhook Logs](actions/list-webhook-logs.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [List Webhooks](actions/list-webhooks.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Mark Interview Finalist](actions/mark-interview-finalist.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Remove Interview Share Link](actions/remove-interview-share-link.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Score Interview](actions/score-interview.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Set Interview External ID](actions/set-interview-external-id.md) | `POST me` | [docs](https://api.hireflix.com/me) |
| [Update Webhook](actions/update-webhook.md) | `POST me` | [docs](https://api.hireflix.com/me) |
