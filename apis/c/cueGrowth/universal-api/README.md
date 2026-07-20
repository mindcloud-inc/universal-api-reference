# <img src="https://images.mindcloud.co/apps/icons/cue-growth_1774988657203.png" alt="CueGrowth logo" width="28" height="28"> CueGrowth: Universal API

CueGrowth helps B2B teams automate LinkedIn outreach, lead generation, campaign management, messaging, and webhook-driven integrations through its public API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cueGrowth/latest
- **Category:** Marketing / Social Media
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cuegrowth.ai
- **Vendor API docs:** https://cuegrowth.ai/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Campaigns](actions/list-campaigns.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET |  |

### Campaigns

| Action | Method | Description |
| --- | --- | --- |
| [Add Receiver To Campaign](actions/add-receiver-to-campaign.md) | PUT |  |
| [Bulk Add Receivers To Campaign](actions/bulk-add-receivers-to-campaign.md) | PUT |  |
| [Get Campaign By Id](actions/get-campaign-by-id.md) | GET |  |
| [List Campaigns by Receiver](actions/list-campaigns-by-receiver.md) | GET |  |
| [Remove Receiver From Campaign](actions/remove-receiver-from-campaign.md) | PUT |  |
| [Update Campaign](actions/update-campaign.md) | PUT |  |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [List Connections](actions/list-connections.md) | GET |  |

### Conversations

| Action | Method | Description |
| --- | --- | --- |
| [Get Inbox](actions/get-inbox.md) | GET |  |
| [List Inboxes](actions/list-inboxes.md) | GET |  |

### Leads

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Receiver](actions/retrieve-receiver.md) | GET |  |

### Messages

| Action | Method | Description |
| --- | --- | --- |
| [List Messages](actions/list-messages.md) | GET |  |
| [Send Message To Inbox](actions/send-message-to-inbox.md) | POST |  |
| [Send Message To Receiver](actions/send-message-to-receiver.md) | POST |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Get Task Status](actions/get-task-status.md) | GET |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET |  |
| [Retrieve User](actions/retrieve-user.md) | GET |  |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |
| [Update Webhook](actions/update-webhook.md) | PUT |  |

