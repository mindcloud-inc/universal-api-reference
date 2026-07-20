# <img src="https://images.mindcloud.co/apps/icons/smart-reach_1774299766469.png" alt="SmartReach logo" width="28" height="28"> SmartReach: Universal API

SmartReach is an all-in-one cold outreach and sales engagement platform for email, LinkedIn, calling, and multichannel prospect workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smartReach/latest
- **Category:** Marketing
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://smartreach.io
- **Vendor API docs:** https://help.smartreach.io/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartReach/latest/actions/list-teams?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create or Update Account](actions/create-or-update-account.md) | POST | Finds an account in SmartReach, or creates one if needed. |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from SmartReach. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from SmartReach. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from SmartReach. |
| [Get Campaign Channel Settings](actions/get-campaign-channel-settings.md) | GET | Retrieves campaign channel settings from SmartReach. |
| [Get Campaign Stats](actions/get-campaign-stats.md) | GET | Retrieves campaign stats from SmartReach. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from SmartReach. |
| [Update Campaign Status](actions/update-campaign-status.md) | PUT | Updates campaign status in SmartReach. |

### Do Not Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add Domains to Do Not Contact List](actions/add-domains-to-do-not-contact-list.md) | POST | Adds domains to the do not contact list in SmartReach. |
| [Add Emails to Do Not Contact List](actions/add-emails-to-do-not-contact-list.md) | POST | Adds emails to the do not contact list in SmartReach. |
| [List Do Not Contact List](actions/list-do-not-contact-list.md) | GET | Retrieves do not contact entries from SmartReach. |
| [Remove Do Not Contact Entries](actions/remove-do-not-contact-entries.md) | DELETE | Deletes do not contact entries from SmartReach. |

### Email Setting

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Setting](actions/get-email-setting.md) | GET | Retrieves an email setting from SmartReach. |
| [List Email Settings](actions/list-email-settings.md) | GET | Retrieves email settings from SmartReach. |

### Prospect

| Action | Method | Description |
| --- | --- | --- |
| [Add or Update Prospects](actions/add-or-update-prospects.md) | POST | Finds prospects in SmartReach, or creates them if needed. |
| [Add Prospects To Campaign](actions/add-prospects-to-campaign.md) | POST | Adds prospects to a campaign in SmartReach. |
| [List Campaign Prospects](actions/list-campaign-prospects.md) | GET | Retrieves campaign prospects from SmartReach. |
| [List Prospects](actions/list-prospects.md) | GET | Retrieves prospects from SmartReach. |
| [Remove Prospects From Campaign](actions/remove-prospects-from-campaign.md) | PUT | Removes prospects from a campaign in SmartReach. |
| [Update Prospect Status](actions/update-prospect-status.md) | PUT | Updates prospect status in SmartReach. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Update Task Status](actions/update-task-status.md) | PUT | Updates task status in SmartReach. |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Get Team](actions/get-team.md) | GET | Retrieves a team from SmartReach. |
| [List Teams](actions/list-teams.md) | GET | Retrieves teams from SmartReach. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from SmartReach. |
| [List Users](actions/list-users.md) | GET | Retrieves users from SmartReach. |

