# <img src="https://images.mindcloud.co/apps/icons/lemlist_1773235908800.png" alt="lemlist logo" width="28" height="28"> lemlist: Universal API

Find leads and automate multichannel outreach with lemlist

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lemlist/latest
- **Category:** Marketing
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.lemlist.com
- **Vendor API docs:** https://developer.lemlist.com/api-reference/getting-started/overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Team Credits](actions/get-team-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/get-team-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | GET | Retrieves your activity records from lemlist. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in lemlist. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a specific campaign from lemlist. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves your campaign list from lemlist. |
| [Pause Campaign](actions/pause-campaign.md) | PUT | Pauses an existing campaign in lemlist. |
| [Start Campaign](actions/start-campaign.md) | PUT | Starts an existing campaign in lemlist. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in lemlist. |

### Campaign Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Stats](actions/get-campaign-stats.md) | GET | Retrieves statistics for a lemlist campaign. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Send Email](actions/send-email.md) | POST | Sends an email from lemlist inbox. |

### Inbox Conversation

| Action | Method | Description |
| --- | --- | --- |
| [List Inboxes](actions/list-inboxes.md) | GET | Retrieves your inbox conversations from lemlist. |

### Inbox Message

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Messages](actions/list-contact-messages.md) | GET | Retrieves contact messages from lemlist inbox. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead in Campaign](actions/create-lead-in-campaign.md) | POST | Creates a new lead in a lemlist campaign. |
| [Get Lead by Email](actions/get-lead-by-email.md) | GET | Finds a lead in lemlist by email address. |
| [List Campaign Leads](actions/list-campaign-leads.md) | GET | Retrieves leads from a lemlist campaign. |
| [Mark Lead as Interested in Campaign](actions/mark-lead-as-interested-in-campaign.md) | PUT | Marks a lead as interested in a lemlist campaign. |
| [Mark Lead as Not Interested in Campaign](actions/mark-lead-as-not-interested-in-campaign.md) | PUT | Marks a lead as not interested in a lemlist campaign. |
| [Pause Lead](actions/pause-lead.md) | PUT | Pauses an existing lead in lemlist. |
| [Resume Paused Lead](actions/resume-paused-lead.md) | PUT | Resumes a paused lead in lemlist. |
| [Update Lead in a Campaign](actions/update-lead-in-a-campaign.md) | PUT | Updates an existing lead in a lemlist campaign. |

### Sequence

| Action | Method | Description |
| --- | --- | --- |
| [List Campaign Sequences](actions/list-campaign-sequences.md) | GET | Retrieves sequences from a lemlist campaign. |

### Team Credits

| Action | Method | Description |
| --- | --- | --- |
| [Get Team Credits](actions/get-team-credits.md) | GET | Retrieves your team credits from lemlist. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Add Webhook](actions/add-webhook.md) | POST | Creates a new webhook in lemlist. |

