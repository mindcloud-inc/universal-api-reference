# <img src="https://images.mindcloud.co/apps/icons/loopedin-icon_1775682402109.png" alt="LoopedIn logo" width="28" height="28"> LoopedIn: Universal API

LoopedIn is product feedback and roadmap software for managing workspaces, roadmaps, roadmap cards, roadmap card features, updates, feedback boards, feedback, and ideas through the official REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/loopedIn/latest
- **Category:** Productivity / Project Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://loopedin.io
- **Vendor API docs:** https://docs.loopedin.io/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/loopedIn/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Details](actions/get-account-details.md) | GET | Retrieves account details from LoopedIn. |

### Feedback

| Action | Method | Description |
| --- | --- | --- |
| [Create Feedback](actions/create-feedback.md) | POST | Creates a new feedback item in LoopedIn. |
| [Delete Feedback](actions/delete-feedback.md) | DELETE | Deletes an existing feedback item from LoopedIn. |
| [Get Feedback](actions/get-feedback.md) | GET | Retrieves a feedback item from LoopedIn. |
| [List Feedback for Board](actions/list-feedback-for-board.md) | GET | Retrieves feedback for a feedback board in LoopedIn. |
| [Update Feedback](actions/update-feedback.md) | PUT | Updates an existing feedback item in LoopedIn. |

### Feedback Board

| Action | Method | Description |
| --- | --- | --- |
| [Get Feedback Board](actions/get-feedback-board.md) | GET | Retrieves a feedback board from LoopedIn. |
| [List Feedback Boards](actions/list-feedback-boards.md) | GET | Retrieves feedback boards from LoopedIn. |

### Idea

| Action | Method | Description |
| --- | --- | --- |
| [Create Idea](actions/create-idea.md) | POST | Creates a new idea in LoopedIn. |
| [List Completed Ideas](actions/list-completed-ideas.md) | GET | Retrieves completed ideas from LoopedIn. |
| [List Ideas](actions/list-ideas.md) | GET | Retrieves ideas from LoopedIn. |
| [List Private Ideas](actions/list-private-ideas.md) | GET | Retrieves private ideas from LoopedIn. |
| [List Public Ideas](actions/list-public-ideas.md) | GET | Retrieves public ideas from LoopedIn. |

### Roadmap

| Action | Method | Description |
| --- | --- | --- |
| [Get Roadmap](actions/get-roadmap.md) | GET | Retrieves a roadmap from LoopedIn. |
| [List Roadmaps](actions/list-roadmaps.md) | GET | Retrieves roadmaps from LoopedIn. |

### Roadmap Card

| Action | Method | Description |
| --- | --- | --- |
| [Create Roadmap Card](actions/create-roadmap-card.md) | POST | Creates a new roadmap card in LoopedIn. |
| [Delete Roadmap Card](actions/delete-roadmap-card.md) | DELETE | Deletes an existing roadmap card from LoopedIn. |
| [Get Roadmap Card](actions/get-roadmap-card.md) | GET | Retrieves a roadmap card from LoopedIn. |
| [List Completed Roadmap Cards](actions/list-completed-roadmap-cards.md) | GET | Retrieves completed roadmap cards from LoopedIn. |
| [List Roadmap Cards](actions/list-roadmap-cards.md) | GET | Retrieves roadmap cards from LoopedIn. |
| [Update Roadmap Card](actions/update-roadmap-card.md) | PUT | Updates an existing roadmap card in LoopedIn. |

### Update

| Action | Method | Description |
| --- | --- | --- |
| [Create Update](actions/create-update.md) | POST | Creates a new update in LoopedIn. |
| [Delete Update](actions/delete-update.md) | DELETE | Deletes an existing update from LoopedIn. |
| [Get Update](actions/get-update.md) | GET | Retrieves an update from LoopedIn. |
| [List Updates](actions/list-updates.md) | GET | Retrieves updates from LoopedIn. |
| [Update Update](actions/update-update.md) | PUT | Updates an existing update in LoopedIn. |

### Update Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Subscribe to Updates](actions/subscribe-to-updates.md) | POST | Subscribes a user to updates in LoopedIn. |
| [Unsubscribe from Updates](actions/unsubscribe-from-updates.md) | DELETE | Unsubscribes a user from updates in LoopedIn. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from LoopedIn. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from LoopedIn. |

