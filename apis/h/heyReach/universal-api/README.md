# <img src="https://images.mindcloud.co/apps/icons/images_1773419719671.jpeg" alt="Hey Reach logo" width="28" height="28"> Hey Reach: Universal API

Manage LinkedIn outreach campaigns, conversations, lists, leads, and webhooks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/heyReach/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.heyreach.io/
- **Vendor API docs:** https://documenter.getpostman.com/view/23808049/2sA2xb5F75

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List LinkedIn Accounts](actions/list-linked-in-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/list-linked-in-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Add Leads To Campaign](actions/add-leads-to-campaign.md) | PUT | Adds leads to a campaign in Hey Reach. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Hey Reach. |
| [List Campaign Leads](actions/list-campaign-leads.md) | GET | Retrieves leads from a Hey Reach campaign. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Hey Reach. |
| [List Campaigns For Lead](actions/list-campaigns-for-lead.md) | GET | Retrieves campaigns for a lead in Hey Reach. |
| [Pause Campaign](actions/pause-campaign.md) | PUT | Pauses a campaign in Hey Reach. |
| [Resume Campaign](actions/resume-campaign.md) | PUT | Resumes a campaign in Hey Reach. |
| [Stop Lead In Campaign](actions/stop-lead-in-campaign.md) | PUT | Stops a lead in a Hey Reach campaign. |

### Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation](actions/get-conversation.md) | GET | Retrieves a LinkedIn conversation from Hey Reach. |
| [List Conversations](actions/list-conversations.md) | GET | Retrieves LinkedIn conversations from Hey Reach. |
| [Send Message](actions/send-message.md) | POST | Sends a message to a LinkedIn conversation in Hey Reach. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Add Lead Tags](actions/add-lead-tags.md) | PUT | Adds tags to a lead in Hey Reach. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from Hey Reach by LinkedIn profile URL. |
| [Get Lead Tags](actions/get-lead-tags.md) | GET | Retrieves tags for a lead in Hey Reach. |
| [Replace Lead Tags](actions/replace-lead-tags.md) | PUT | Replaces tags for a lead in Hey Reach. |

### Lead Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead Tags](actions/create-lead-tags.md) | POST | Creates lead tags in Hey Reach. |

### Linkedin Account

| Action | Method | Description |
| --- | --- | --- |
| [List LinkedIn Accounts](actions/list-linked-in-accounts.md) | GET | Retrieves LinkedIn accounts from Hey Reach. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Add Leads To List](actions/add-leads-to-list.md) | PUT | Adds leads to a list in Hey Reach. |
| [Create Empty List](actions/create-empty-list.md) | POST | Creates an empty lead or company list in Hey Reach. |
| [Get List](actions/get-list.md) | GET | Retrieves a lead or company list from Hey Reach. |
| [List Companies In List](actions/list-companies-in-list.md) | GET | Retrieves companies from a Hey Reach list. |
| [List Leads In List](actions/list-leads-in-list.md) | GET | Retrieves leads from a Hey Reach list. |
| [List Lists](actions/list-lists.md) | GET | Retrieves lead and company lists from Hey Reach. |
| [List Lists For Lead](actions/list-lists-for-lead.md) | GET | Retrieves lists for a lead in Hey Reach. |

### Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Overall Stats](actions/get-overall-stats.md) | GET | Retrieves overall stats from Hey Reach. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Hey Reach. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Hey Reach. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Hey Reach. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Hey Reach. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Hey Reach. |

