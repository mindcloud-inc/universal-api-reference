# <img src="https://images.mindcloud.co/apps/icons/linkedcamp-icon_1776781405673.png" alt="LinkedCamp logo" width="28" height="28"> LinkedCamp: Universal API

LinkedCamp is a LinkedIn and email outreach automation platform for creating and running prospecting campaigns.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/linkedCamp/latest
- **Category:** Marketing
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://linkedcamp.com
- **Vendor API docs:** https://api.linkedcamp.com/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account API Token](actions/get-account-api-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedCamp/latest/actions/get-account-api-token?connectionId=$CONNECTION_ID&accountEmail=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Api Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Account API Token](actions/get-account-api-token.md) | GET |  |
| [Get User Token](actions/get-user-token.md) | GET |  |

### Blacklist Entry

| Action | Method | Description |
| --- | --- | --- |
| [Add Blacklist Entry](actions/add-blacklist-entry.md) | POST |  |
| [List Blacklist Entries](actions/list-blacklist-entries.md) | GET |  |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | POST |  |
| [Create Connect Campaign](actions/create-connect-campaign.md) | POST |  |
| [Create Email Campaign](actions/create-email-campaign.md) | POST |  |
| [Create InMail Campaign](actions/create-inmail-campaign.md) | POST |  |
| [Create Message Campaign](actions/create-message-campaign.md) | POST |  |
| [Get Campaign](actions/get-campaign.md) | GET |  |
| [List Campaigns](actions/list-campaigns.md) | GET |  |
| [Update Campaign Status](actions/update-campaign-status.md) | PUT |  |

### Campaign Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Stats](actions/get-campaign-stats.md) | GET |  |

### Conversation Message

| Action | Method | Description |
| --- | --- | --- |
| [Get Conversation Messages](actions/get-conversation-messages.md) | GET |  |
| [Send Conversation Message](actions/send-conversation-message.md) | POST |  |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Add Leads To Campaign](actions/add-leads-to-campaign.md) | POST |  |
| [Get Lead](actions/get-lead.md) | GET |  |
| [List Campaign Leads](actions/list-campaign-leads.md) | GET |  |
| [Update Lead](actions/update-lead.md) | PUT |  |
| [Update Lead Campaign Status](actions/update-lead-campaign-status.md) | PUT |  |

### Sub-account

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Sub-Account](actions/cancel-sub-account.md) | DELETE |  |
| [Pause Sub-Account](actions/pause-sub-account.md) | PUT |  |
| [Register Sub-Account](actions/register-sub-account.md) | POST |  |
| [Resume Sub-Account](actions/resume-sub-account.md) | PUT |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST |  |
| [List Tags](actions/list-tags.md) | GET |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST |  |
| [Delete Webhook](actions/delete-webhook.md) | DELETE |  |
| [Get Webhook](actions/get-webhook.md) | GET |  |
| [List Webhooks](actions/list-webhooks.md) | GET |  |

