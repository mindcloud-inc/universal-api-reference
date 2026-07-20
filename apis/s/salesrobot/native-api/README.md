# Salesrobot: Native API Reference

A consolidated summary of Salesrobot's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb
- **API base URL:** `https://api.boomtechinc.com`

## Authentication

### API Key

Connect with a SalesRobot API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-API-KEY: <apiKey>
```

[Official authentication documentation](https://salesrobot.crisp.help/en/article/using-salesrobot-apis-twsjff/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `size` in the query string to set the page size (default 20). Use `page` in the query string to choose the page; numbering starts at 0.

## Sorting

Set the sort field with `sort` in the query string. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Campaign Sequence Steps](actions/add-campaign-sequence-steps.md) | `POST /api/sequence/save/from-steps` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Add Single Prospect](actions/add-single-prospect.md) | `POST /api/add-single-prospect` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Check LinkedIn Email Availability](actions/check-linked-in-email-availability.md) | `POST /api/linkedin_account/check_email` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Copy Blacklist From LinkedIn Account](actions/copy-blacklist-from-linked-in-account.md) | `POST /api/blacklist/copy_from_account` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Create AI Variable](actions/create-ai-variable.md) | `POST /api/sequence/add_new_ai_variable` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Create Campaign](actions/create-campaign.md) | `POST /api/campaign` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Delete Prospects](actions/delete-prospects.md) | `POST /api/campaign/deleteMultiple` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Get Campaign Stats](actions/get-campaign-stats.md) | `GET /api/campaignTimeWiseStats` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Get LinkedIn Auth URL](actions/get-linked-in-auth-url.md) | `POST /api/linkedin/account/auth` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Get LinkedIn Posts](actions/get-linked-in-posts.md) | `GET /api/linkedin/posts` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Get LinkedIn Profile Data](actions/get-linked-in-profile-data.md) | `GET /api/linkedin/profile/:publicIdentifier` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Get Prospect Status](actions/get-prospect-status.md) | `GET /api/campaign/prospects/execution-details` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Get Stats Range](actions/get-stats-range.md) | `POST /api/campaign/stats` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Import Prospects From CSV](actions/import-prospects-from-csv.md) | `POST /api/add-from-csv` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Import Prospects From LinkedIn URL](actions/import-prospects-from-linked-in-url.md) | `POST /api/add-from-lisalesnav-search` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [List AI Variables](actions/list-ai-variables.md) | `GET /api/sequence/ai_variable` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [List Campaign Prospects](actions/list-campaign-prospects.md) | `GET /api/campaign/prospects` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [List Campaigns](actions/list-campaigns.md) | `GET /api/campaigns` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [List LinkedIn Accounts](actions/list-linked-in-accounts.md) | `GET /api/linkedinAccounts` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Pause Or Resume Campaign](actions/pause-or-resume-campaign.md) | `POST /api/campaign/pause` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Pause Prospect](actions/pause-prospect.md) | `POST /api/campaign/pauseForProspect` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Post LinkedIn Job](actions/post-linked-in-job.md) | `POST /api/linkedin/jobs` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Start Campaign](actions/start-campaign.md) | `POST /api/start` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Sync LinkedIn Inbox](actions/sync-linked-in-inbox.md) | `POST /api/syncedMessages` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Tag Chat](actions/tag-chat.md) | `POST /api/messageTags` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Update Blacklist](actions/update-blacklist.md) | `POST /api/blacklist/update` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Update Campaign Configuration](actions/update-campaign-configuration.md) | `POST /api/campaign/settings/update` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Update Daily Quotas](actions/update-daily-quotas.md) | `POST /api/settings/quota` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Update Pending Invite Settings](actions/update-pending-invite-settings.md) | `POST /api/settings/pendingInvite` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
| [Update Schedule](actions/update-schedule.md) | `POST /api/schedule` | [docs](https://documenter.getpostman.com/view/10815846/2sB3BKE8Fb) |
