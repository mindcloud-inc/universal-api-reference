# <img src="https://images.mindcloud.co/apps/icons/elmah-icon_1775666800603.png" alt="elmah.io logo" width="28" height="28"> elmah.io: Universal API

Monitor errors, logs, deployments, heartbeats, and uptime checks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/elmahio/latest
- **Category:** IT Operations / Observability
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://elmah.io
- **Vendor API docs:** https://docs.elmah.io/using-the-rest-api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Logs](actions/list-logs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elmahio/latest/actions/list-logs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Create Log](actions/create-log.md) | POST | Creates a new log in elmah.io. |
| [Delete Log](actions/delete-log.md) | DELETE | Deletes an existing log from elmah.io. |
| [Diagnose Log](actions/diagnose-log.md) | GET | Retrieves log diagnostics from elmah.io. |
| [Disable Log](actions/disable-log.md) | PUT | Disables a log in elmah.io. |
| [Enable Log](actions/enable-log.md) | PUT | Enables a log in elmah.io. |
| [Get Log](actions/get-log.md) | GET | Retrieves a log from elmah.io. |
| [List Logs](actions/list-logs.md) | GET | Retrieves logs from elmah.io. |

### Deployments

| Action | Method | Description |
| --- | --- | --- |
| [Create Deployment](actions/create-deployment.md) | POST | Creates a new deployment in elmah.io. |
| [Delete Deployment](actions/delete-deployment.md) | DELETE | Deletes an existing deployment from elmah.io. |
| [Get Deployment](actions/get-deployment.md) | GET | Retrieves a deployment from elmah.io. |
| [List Deployments](actions/list-deployments.md) | GET | Retrieves deployments from elmah.io. |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [Create Message](actions/create-message.md) | POST | Creates a new message in elmah.io. |
| [Create Messages Bulk](actions/create-messages-bulk.md) | POST | Creates one or more messages in elmah.io. |
| [Delete Message](actions/delete-message.md) | DELETE | Deletes an existing message from elmah.io. |
| [Delete Messages](actions/delete-messages.md) | DELETE | Deletes messages from a log in elmah.io. |
| [Fix Message](actions/fix-message.md) | PUT | Marks a message as fixed in elmah.io. |
| [Fix Messages](actions/fix-messages.md) | PUT | Marks messages as fixed in elmah.io. |
| [Get Message](actions/get-message.md) | GET | Retrieves a message from elmah.io. |
| [Hide Message](actions/hide-message.md) | PUT | Hides a message in elmah.io. |
| [List Messages](actions/list-messages.md) | GET | Retrieves messages from a log in elmah.io. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Create Heartbeat](actions/create-heartbeat.md) | POST | Creates a new heartbeat in elmah.io. |

