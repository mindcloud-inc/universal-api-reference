# <img src="https://images.mindcloud.co/apps/icons/favicon-documenter-getpostman-com-48x48_1775763570048.png" alt="Salesrobot logo" width="28" height="28"> Salesrobot: Universal API

Automate LinkedIn outreach, email campaigns, and lead follow-up

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/salesrobot/latest
- **Category:** Marketing
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://salesrobot.co
- **Vendor API docs:** https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List LinkedIn Accounts](actions/list-linked-in-accounts.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesrobot/latest/actions/list-linked-in-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Ai Variable

| Action | Method | Description |
| --- | --- | --- |
| [Create AI Variable](actions/create-ai-variable.md) | POST |  |
| [List AI Variables](actions/list-ai-variables.md) | GET |  |

### Blacklist

| Action | Method | Description |
| --- | --- | --- |
| [Copy Blacklist From LinkedIn Account](actions/copy-blacklist-from-linked-in-account.md) | PUT |  |
| [Update Blacklist](actions/update-blacklist.md) | PUT |  |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Add Campaign Sequence Steps](actions/add-campaign-sequence-steps.md) | PUT |  |
| [Create Campaign](actions/create-campaign.md) | POST |  |
| [List Campaigns](actions/list-campaigns.md) | GET |  |
| [Pause Or Resume Campaign](actions/pause-or-resume-campaign.md) | PUT |  |
| [Start Campaign](actions/start-campaign.md) | PUT |  |
| [Update Campaign Configuration](actions/update-campaign-configuration.md) | PUT |  |

### Campaign Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Stats](actions/get-campaign-stats.md) | GET |  |

### Inbox

| Action | Method | Description |
| --- | --- | --- |
| [Sync LinkedIn Inbox](actions/sync-linked-in-inbox.md) | PUT |  |

### Inbox Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Tag Chat](actions/tag-chat.md) | PUT |  |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Post LinkedIn Job](actions/post-linked-in-job.md) | POST |  |

### Linkedin Account

| Action | Method | Description |
| --- | --- | --- |
| [Check LinkedIn Email Availability](actions/check-linked-in-email-availability.md) | GET |  |
| [Get LinkedIn Auth URL](actions/get-linked-in-auth-url.md) | POST |  |
| [List LinkedIn Accounts](actions/list-linked-in-accounts.md) | GET |  |
| [Update Daily Quotas](actions/update-daily-quotas.md) | PUT |  |
| [Update Pending Invite Settings](actions/update-pending-invite-settings.md) | PUT |  |

### Linkedin Post

| Action | Method | Description |
| --- | --- | --- |
| [Get LinkedIn Posts](actions/get-linked-in-posts.md) | GET |  |

### Linkedin Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get LinkedIn Profile Data](actions/get-linked-in-profile-data.md) | GET |  |

### Prospect

| Action | Method | Description |
| --- | --- | --- |
| [Add Single Prospect](actions/add-single-prospect.md) | POST |  |
| [Delete Prospects](actions/delete-prospects.md) | DELETE |  |
| [Get Prospect Status](actions/get-prospect-status.md) | GET |  |
| [Import Prospects From CSV](actions/import-prospects-from-csv.md) | POST |  |
| [Import Prospects From LinkedIn URL](actions/import-prospects-from-linked-in-url.md) | POST |  |
| [List Campaign Prospects](actions/list-campaign-prospects.md) | GET |  |
| [Pause Prospect](actions/pause-prospect.md) | PUT |  |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Update Schedule](actions/update-schedule.md) | PUT |  |

### Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Stats Range](actions/get-stats-range.md) | GET |  |

