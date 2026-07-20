# <img src="https://images.mindcloud.co/apps/icons/973459ed-d7b9-4fc0-a5f8-ed14cbfe6e86-5_1775668424009.png" alt="UserVitals logo" width="28" height="28"> UserVitals: Universal API

Collect product feedback, manage idea backlogs, and share a public roadmap with launch updates.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/userVitals/latest
- **Category:** Productivity / Project Management
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://roadmap.space/
- **Vendor API docs:** https://api.roadmap.space/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Roadmap](actions/get-roadmap.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/get-roadmap?connectionId=$CONNECTION_ID&roadmapId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Attach Feedback To Existing Item](actions/attach-feedback-to-existing-item.md) | PUT | Attaches feedback to an existing idea or story. |
| [Convert Feedback To Idea](actions/convert-feedback-to-idea.md) | PUT | Converts a feedback item to an idea. |
| [Create Feedback](actions/create-feedback.md) | POST | Creates a new feedback item in the roadmap API. |
| [Delete Feedback](actions/delete-feedback.md) | DELETE | Deletes a feedback item from the roadmap API. |
| [List Feedback](actions/list-feedback.md) | GET | Retrieves feedback items for a roadmap from the roadmap API. |
| [Unlink Feedback](actions/unlink-feedback.md) | DELETE | Unlinks feedback from a parent idea or story. |
| [Update Feedback](actions/update-feedback.md) | PUT | Updates an existing feedback item in the roadmap API. |

### Idea

| Action | Method | Description |
| --- | --- | --- |
| [Archive Idea](actions/archive-idea.md) | DELETE | Archives an idea in the roadmap API. |
| [Create Idea](actions/create-idea.md) | POST | Creates a new idea in the roadmap API. |
| [Get Widget Ideas](actions/get-widget-ideas.md) | GET | Retrieves widget ideas for a roadmap from the roadmap API. |
| [List Ideas](actions/list-ideas.md) | GET | Retrieves ideas for a roadmap from the roadmap API. |
| [Move Idea](actions/move-idea.md) | PUT | Moves an idea to another roadmap state. |
| [Update Idea](actions/update-idea.md) | PUT | Updates an existing idea in the roadmap API. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Item](actions/get-item.md) | GET | Retrieves an item by token from the roadmap API. |

### Roadmap

| Action | Method | Description |
| --- | --- | --- |
| [Get Roadmap](actions/get-roadmap.md) | GET | Retrieves a roadmap by ID from the roadmap API. |

### Story

| Action | Method | Description |
| --- | --- | --- |
| [Attach Item To Story](actions/attach-item-to-story.md) | PUT | Attaches an idea or feedback item to a story. |
| [Create Story](actions/create-story.md) | POST | Creates a new story in the roadmap API. |
| [Delete Story](actions/delete-story.md) | DELETE | Deletes a story from the roadmap API. |
| [List Stories](actions/list-stories.md) | GET | Retrieves stories for a roadmap from the roadmap API. |
| [Update Story](actions/update-story.md) | PUT | Updates an existing story in the roadmap API. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Webhook](actions/cancel-webhook.md) | DELETE | Cancels a webhook in the roadmap API. |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in the roadmap API. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from the roadmap API. |

