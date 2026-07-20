# <img src="https://images.mindcloud.co/apps/icons/cloud-bot-icon-filled-256_1774639991536.png" alt="Cloud BOT logo" width="28" height="28"> Cloud BOT: Universal API

Cloud BOT is a fully cloud-based RPA service that records browser operations and exposes BOT execution, job, subscription, file, and contract APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloudBOT/latest
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.c-bot.pro/en/
- **Vendor API docs:** https://docs.c-bot.pro/en/api_reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Contracts](actions/list-contracts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/list-contracts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Contracts

| Action | Method | Description |
| --- | --- | --- |
| [Issue WS Token](actions/issue-ws-token.md) | GET | Issues a WebSocket token in Cloud BOT. |
| [List Contracts](actions/list-contracts.md) | GET | Retrieves contracts from Cloud BOT. |

### Workflow Runs

| Action | Method | Description |
| --- | --- | --- |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from Cloud BOT. |
| [List Bot Jobs](actions/list-bot-jobs.md) | GET | Retrieves bot jobs from Cloud BOT. |
| [Run Bot](actions/run-bot.md) | POST | Creates a bot job in Cloud BOT. |
| [Suspend Job](actions/suspend-job.md) | DELETE | Deletes a job from Cloud BOT. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [Create Bot Subscription](actions/create-bot-subscription.md) | POST | Creates a bot subscription in Cloud BOT. |
| [Delete Bot Subscription](actions/delete-bot-subscription.md) | DELETE | Deletes a bot subscription from Cloud BOT. |
| [Export Bot Definition](actions/export-bot-definition.md) | GET | Retrieves a bot definition from Cloud BOT. |
| [Get Bot Details](actions/get-bot-details.md) | GET | Retrieves bot details from Cloud BOT. |
| [List Bot Subscriptions](actions/list-bot-subscriptions.md) | GET | Retrieves bot subscriptions from Cloud BOT. |
| [List Bots](actions/list-bots.md) | GET | Retrieves bots from Cloud BOT. |

