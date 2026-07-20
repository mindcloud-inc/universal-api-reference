# UserVitals: Native API Reference

A consolidated summary of UserVitals's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://api.roadmap.space/
- **API base URL:** `https://app.roadmap.space/v1`

## Authentication

### Basic Auth

Use your Roadmap account email as the username and a Personal Access Token as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://api.roadmap.space/#authentication)

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Idea](actions/archive-idea.md) | `DELETE /ideas/:publicItemTokenId` | [docs](https://api.roadmap.space/#archive-idea) |
| [Attach Feedback To Existing Item](actions/attach-feedback-to-existing-item.md) | `POST /feedback/attach` | [docs](https://api.roadmap.space/#attach-to-existing-idea-or-story) |
| [Attach Item To Story](actions/attach-item-to-story.md) | `POST /stories/ideas` | [docs](https://api.roadmap.space/#attach) |
| [Cancel Webhook](actions/cancel-webhook.md) | `POST /webhooks/cancel` | [docs](https://api.roadmap.space/#cancel-a-webhook) |
| [Convert Feedback To Idea](actions/convert-feedback-to-idea.md) | `PUT /feedback/convert` | [docs](https://api.roadmap.space/#convert-feedback-to-idea) |
| [Create Feedback](actions/create-feedback.md) | `POST /feedback` | [docs](https://api.roadmap.space/#create-feedback) |
| [Create Idea](actions/create-idea.md) | `POST /ideas` | [docs](https://api.roadmap.space/#create-idea) |
| [Create Story](actions/create-story.md) | `POST /stories` | [docs](https://api.roadmap.space/#create-story) |
| [Create Webhook](actions/create-webhook.md) | `POST /webhooks` | [docs](https://api.roadmap.space/#create-webhook) |
| [Delete Feedback](actions/delete-feedback.md) | `DELETE /feedback/:publicItemTokenId` | [docs](https://api.roadmap.space/#delete-feedback) |
| [Delete Story](actions/delete-story.md) | `DELETE /stories/:publicItemTokenId` | [docs](https://api.roadmap.space/#delete-story) |
| [Get Item](actions/get-item.md) | `GET /items/:publicItemTokenId` | [docs](https://api.roadmap.space/#get-item) |
| [Get Roadmap](actions/get-roadmap.md) | `GET /roadmaps/:id` | [docs](https://api.roadmap.space/) |
| [Get Widget Ideas](actions/get-widget-ideas.md) | `GET /roadmaps/:id/widget` | [docs](https://api.roadmap.space/#get-widget-ideas) |
| [List Feedback](actions/list-feedback.md) | `GET /feedback/list/:roadmapId` | [docs](https://api.roadmap.space/#list-feedback) |
| [List Ideas](actions/list-ideas.md) | `GET /ideas/list/:roadmapId` | [docs](https://api.roadmap.space/#list-idea) |
| [List Stories](actions/list-stories.md) | `GET /stories/:roadmapId` | [docs](https://api.roadmap.space/#list-story) |
| [List Webhooks](actions/list-webhooks.md) | `GET /webhooks` | [docs](https://api.roadmap.space/#get-webhooks) |
| [Move Idea](actions/move-idea.md) | `POST /ideas/move/:type` | [docs](https://api.roadmap.space/#move-to-widget-idea-active) |
| [Unlink Feedback](actions/unlink-feedback.md) | `DELETE /feedback/:publicItemTokenId/unlink/:parentId` | [docs](https://api.roadmap.space/#unlink-feedback) |
| [Update Feedback](actions/update-feedback.md) | `PUT /ideas` | [docs](https://api.roadmap.space/#update-feedback) |
| [Update Idea](actions/update-idea.md) | `PUT /ideas` | [docs](https://api.roadmap.space/#update-idea) |
| [Update Story](actions/update-story.md) | `PUT /stories` | [docs](https://api.roadmap.space/#update-story) |
