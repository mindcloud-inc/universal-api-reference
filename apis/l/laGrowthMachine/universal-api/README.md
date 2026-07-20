# LaGrowthMachine: Universal API

Multichannel outbound sales automation platform for campaigns, leads, audiences, inbox workflows, and prospecting operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/laGrowthMachine/latest
- **Category:** Marketing
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lagrowthmachine.com/
- **Vendor API docs:** https://documenter.getpostman.com/view/2071164/TVCmSkH2

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Members](actions/list-members.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/laGrowthMachine/latest/actions/list-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Audience

| Action | Method | Description |
| --- | --- | --- |
| [Create Audience from LinkedIn URL](actions/create-audience-from-linked-in-url.md) | POST | Creates an audience in LaGrowthMachine from a LinkedIn URL. |
| [List Audiences](actions/list-audiences.md) | GET | Retrieves audiences from LaGrowthMachine. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from LaGrowthMachine. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from LaGrowthMachine. |

### Campaign Lead Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Lead Stats](actions/get-campaign-lead-stats.md) | GET | Retrieves campaign lead stats from LaGrowthMachine. |

### Campaign Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Stats](actions/get-campaign-stats.md) | GET | Retrieves campaign stats from LaGrowthMachine. |

### Conversation Note

| Action | Method | Description |
| --- | --- | --- |
| [Edit Inbox Conversation Note](actions/edit-inbox-conversation-note.md) | PUT | Updates an inbox conversation note in LaGrowthMachine. |

### Identity

| Action | Method | Description |
| --- | --- | --- |
| [List Identities](actions/list-identities.md) | GET | Retrieves identities from LaGrowthMachine. |

### Inbox Message

| Action | Method | Description |
| --- | --- | --- |
| [Send Email Message](actions/send-email-message.md) | POST | Sends an email message to a lead in LaGrowthMachine. |
| [Send LinkedIn Message](actions/send-linked-in-message.md) | POST | Sends a LinkedIn message to a lead in LaGrowthMachine. |

### Inbox Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Inbox Webhook](actions/create-inbox-webhook.md) | POST | Creates an inbox webhook in LaGrowthMachine. |
| [Delete Inbox Webhook](actions/delete-inbox-webhook.md) | DELETE | Deletes an inbox webhook from LaGrowthMachine. |
| [List Inbox Webhooks](actions/list-inbox-webhooks.md) | GET | Retrieves inbox webhooks from LaGrowthMachine. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Lead](actions/create-or-update-lead.md) | PUT | Creates or updates a lead in LaGrowthMachine. |
| [Remove Lead from Audiences](actions/remove-lead-from-audiences.md) | PUT | Removes a lead from audiences in LaGrowthMachine. |
| [Search Leads](actions/search-leads.md) | GET | Finds leads in LaGrowthMachine. |
| [Update Lead Status](actions/update-lead-status.md) | PUT | Updates a lead's status in LaGrowthMachine. |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [List Members](actions/list-members.md) | GET | Retrieves members from LaGrowthMachine. |

