# <img src="https://images.mindcloud.co/apps/icons/logo-browse-ai_1773424852194.png" alt="Browse AI logo" width="28" height="28"> Browse AI: Universal API

Browse AI: Run robots, monitor websites, and manage scraped data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/browseAI/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 19
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://browse.ai/
- **Vendor API docs:** https://developers.browse.ai/v2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Robots](actions/list-robots.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/browseAI/latest/actions/list-robots?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (19)

### Bulk Run

| Action | Method | Description |
| --- | --- | --- |
| [Get Bulk Run](actions/get-bulk-run.md) | GET | Retrieves a bulk run from Browse AI. |
| [List Bulk Runs](actions/list-bulk-runs.md) | GET | Retrieves bulk runs from Browse AI. |
| [Start Bulk Run](actions/start-bulk-run.md) | POST | Starts a bulk run in Browse AI. |

### Monitor

| Action | Method | Description |
| --- | --- | --- |
| [Create Monitor](actions/create-monitor.md) | POST | Creates a monitor in Browse AI. |
| [Delete Monitor](actions/delete-monitor.md) | DELETE | Deletes a monitor from Browse AI. |
| [Get Monitor](actions/get-monitor.md) | GET | Retrieves a monitor from Browse AI. |
| [List Monitors](actions/list-monitors.md) | GET | Retrieves monitors from Browse AI. |
| [Update Monitor](actions/update-monitor.md) | PUT | Updates an existing monitor in Browse AI. |

### Robot

| Action | Method | Description |
| --- | --- | --- |
| [Get Robot](actions/get-robot.md) | GET | Retrieves a robot from Browse AI. |
| [List Robots](actions/list-robots.md) | GET | Retrieves robots from Browse AI. |

### Robot Cookie

| Action | Method | Description |
| --- | --- | --- |
| [Update Robot Cookies](actions/update-robot-cookies.md) | PUT | Updates robot cookies in Browse AI. |

### Robot Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Robot Task](actions/get-robot-task.md) | GET | Retrieves a robot task from Browse AI. |
| [List Robot Tasks](actions/list-robot-tasks.md) | GET | Retrieves robot tasks from Browse AI. |
| [Run Robot Task](actions/run-robot-task.md) | POST | Runs a robot task in Browse AI. |

### System

| Action | Method | Description |
| --- | --- | --- |
| [Check System Status](actions/check-system-status.md) | GET | Retrieves system status from Browse AI. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in Browse AI. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Browse AI. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Browse AI. |

