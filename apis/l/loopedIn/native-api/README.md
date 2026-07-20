# LoopedIn: Native API Reference

A consolidated summary of LoopedIn's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.loopedin.io/
- **API base URL:** `https://api.loopedin.io/v1`

## Authentication

### API Key

Use a LoopedIn personal API key sent as Authorization: Bearer <API_KEY>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.loopedin.io/#authentication)

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Feedback](actions/create-feedback.md) | `POST /feedback` | [docs](https://docs.loopedin.io/#feedback) |
| [Create Idea](actions/create-idea.md) | `POST /ideas` | [docs](https://docs.loopedin.io/#create-idea) |
| [Create Roadmap Card](actions/create-roadmap-card.md) | `POST /roadmap-cards` | [docs](https://docs.loopedin.io/#create-roadmap-card) |
| [Create Update](actions/create-update.md) | `POST /updates` | [docs](https://docs.loopedin.io/#create-update) |
| [Delete Feedback](actions/delete-feedback.md) | `DELETE /feedback/:id` | [docs](https://docs.loopedin.io/#feedback) |
| [Delete Roadmap Card](actions/delete-roadmap-card.md) | `DELETE /roadmap-cards/:id` | [docs](https://docs.loopedin.io/#roadmap-cards) |
| [Delete Update](actions/delete-update.md) | `DELETE /updates/:id` | [docs](https://docs.loopedin.io/#delete-update) |
| [Get Account Details](actions/get-account-details.md) | `GET /account` | [docs](https://docs.loopedin.io/#get-account-details) |
| [Get Feedback](actions/get-feedback.md) | `GET /feedback/:id` | [docs](https://docs.loopedin.io/#get-feedback) |
| [Get Feedback Board](actions/get-feedback-board.md) | `GET /feedback-boards/:id` | [docs](https://docs.loopedin.io/#get-feedback-board) |
| [Get Roadmap](actions/get-roadmap.md) | `GET /roadmaps/:id` | [docs](https://docs.loopedin.io/#get-roadmap) |
| [Get Roadmap Card](actions/get-roadmap-card.md) | `GET /roadmap-cards/:id` | [docs](https://docs.loopedin.io/#get-roadmap-card) |
| [Get Update](actions/get-update.md) | `GET /updates/:id` | [docs](https://docs.loopedin.io/#get-update) |
| [Get Workspace](actions/get-workspace.md) | `GET /workspaces/:id` | [docs](https://docs.loopedin.io/#get-workspace) |
| [List Completed Ideas](actions/list-completed-ideas.md) | `GET /ideas` | [docs](https://docs.loopedin.io/#get-all-ideas) |
| [List Completed Roadmap Cards](actions/list-completed-roadmap-cards.md) | `GET /roadmap-cards` | [docs](https://docs.loopedin.io/#get-all-roadmap-cards) |
| [List Feedback Boards](actions/list-feedback-boards.md) | `GET /feedback-boards` | [docs](https://docs.loopedin.io/#get-all-feedback-boards) |
| [List Feedback for Board](actions/list-feedback-for-board.md) | `GET /feedback-boards/:id/feedback` | [docs](https://docs.loopedin.io/#get-all-feedback-for-a-given-feedback-board) |
| [List Ideas](actions/list-ideas.md) | `GET /ideas` | [docs](https://docs.loopedin.io/#get-all-ideas) |
| [List Private Ideas](actions/list-private-ideas.md) | `GET /ideas` | [docs](https://docs.loopedin.io/#get-all-ideas) |
| [List Public Ideas](actions/list-public-ideas.md) | `GET /ideas` | [docs](https://docs.loopedin.io/#get-all-ideas) |
| [List Roadmap Cards](actions/list-roadmap-cards.md) | `GET /roadmap-cards` | [docs](https://docs.loopedin.io/#get-all-roadmap-cards) |
| [List Roadmaps](actions/list-roadmaps.md) | `GET /roadmaps` | [docs](https://docs.loopedin.io/#get-all-roadmaps) |
| [List Updates](actions/list-updates.md) | `GET /updates` | [docs](https://docs.loopedin.io/#get-all-updates) |
| [List Workspaces](actions/list-workspaces.md) | `GET /workspaces` | [docs](https://docs.loopedin.io/#get-all-workspaces) |
| [Subscribe to Updates](actions/subscribe-to-updates.md) | `POST /updates/public-subscribe` | [docs](https://docs.loopedin.io/#subscribe-to-updates) |
| [Unsubscribe from Updates](actions/unsubscribe-from-updates.md) | `POST /updates/public-unsubscribe` | [docs](https://docs.loopedin.io/#unsubscribe-from-updates) |
| [Update Feedback](actions/update-feedback.md) | `PUT /feedback/:id` | [docs](https://docs.loopedin.io/#feedback) |
| [Update Roadmap Card](actions/update-roadmap-card.md) | `PUT /roadmap-cards/:id` | [docs](https://docs.loopedin.io/#update-roadmap-card) |
| [Update Update](actions/update-update.md) | `PUT /updates/:id` | [docs](https://docs.loopedin.io/#update-update) |
