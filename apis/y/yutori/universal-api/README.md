# <img src="https://images.mindcloud.co/apps/icons/yutori_1776185612734.png" alt="Yutori logo" width="28" height="28"> Yutori: Universal API

Run web agents, browsing tasks, research, and scouts

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/yutori/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://yutori.com
- **Vendor API docs:** https://docs.yutori.com

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Health](actions/get-health.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/yutori/latest/actions/get-health?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Browsing Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Browsing Task](actions/create-browsing-task.md) | POST | Creates a Yutori browsing task for an automated web workflow. |
| [Get Browsing Task Status](actions/get-browsing-task-status.md) | GET | Retrieves the status and results of a Yutori browsing task. |

### Browsing Task Trajectory

| Action | Method | Description |
| --- | --- | --- |
| [Download Browsing Task Trajectory](actions/download-browsing-task-trajectory.md) | GET | Downloads the trajectory of a completed Yutori browsing task. |

### Chat Completion

| Action | Method | Description |
| --- | --- | --- |
| [Create Chat Completion](actions/create-chat-completion.md) | POST | Creates a chat completion in Yutori. |

### Email Settings

| Action | Method | Description |
| --- | --- | --- |
| [Update Scout Email Settings](actions/update-scout-email-settings.md) | PUT | Updates email settings and subscribers for a scout in Yutori. |

### Health

| Action | Method | Description |
| --- | --- | --- |
| [Get Health](actions/get-health.md) | GET | Retrieves the current Yutori API health status. |

### Research Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Research Task](actions/create-research-task.md) | POST | Creates a one-time research task in Yutori. |
| [Get Research Task Result](actions/get-research-task-result.md) | GET | Retrieves the status and results of a Yutori research task. |

### Scout

| Action | Method | Description |
| --- | --- | --- |
| [Create Scout](actions/create-scout.md) | POST | Creates a new scout in Yutori. |
| [Delete Scout](actions/delete-scout.md) | DELETE | Deletes an existing scout from Yutori. |
| [Get Scout](actions/get-scout.md) | GET | Retrieves details for a specific scout in Yutori. |
| [List Scouts](actions/list-scouts.md) | GET | Retrieves scouting tasks for the current Yutori account. |
| [Mark Scout Complete](actions/mark-scout-complete.md) | PUT | Marks a Yutori scout as complete. |
| [Mark Scout Done](actions/mark-scout-done.md) | PUT | Marks a Yutori scout as done and archives it. |
| [Partially Update Scout](actions/partially-update-scout.md) | PUT | Updates specific fields of an existing scout in Yutori. |
| [Pause Scout](actions/pause-scout.md) | PUT | Pauses an active scout in Yutori. |
| [Restart Scout](actions/restart-scout.md) | PUT | Restarts an existing scout in Yutori. |
| [Resume Scout](actions/resume-scout.md) | PUT | Resumes a paused scout in Yutori. |
| [Update Scout](actions/update-scout.md) | PUT | Updates an existing scout in Yutori. |

### Scout Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Subscribe to Scout](actions/bulk-subscribe-to-scout.md) | POST | Creates email subscriptions for a scout in Yutori. |
| [Get Scout Subscriptions](actions/get-scout-subscriptions.md) | GET | Retrieves subscriptions for a specific scout in Yutori. |
| [Subscribe to Scout](actions/subscribe-to-scout.md) | POST | Creates a subscription for a scout in Yutori. |
| [Unsubscribe from Scout](actions/unsubscribe-from-scout.md) | DELETE | Deletes a subscription from a scout in Yutori. |

### Scout Update

| Action | Method | Description |
| --- | --- | --- |
| [Get All Scout Updates](actions/get-all-scout-updates.md) | GET | Retrieves updates across all Yutori scouts. |
| [Get Scout Updates](actions/get-scout-updates.md) | GET | Retrieves updates for a specific scout in Yutori. |

### Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Usage](actions/get-usage.md) | GET | Retrieves Yutori account usage, active scouts, and rate limits. |

### Webhook Test

| Action | Method | Description |
| --- | --- | --- |
| [Test Scout Webhook](actions/test-scout-webhook.md) | POST | Creates a test request for a Yutori scout webhook. |

