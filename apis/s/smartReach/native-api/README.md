# SmartReach: Native API Reference

A consolidated summary of SmartReach's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://help.smartreach.io/reference
- **OpenAPI specification:** https://dash.readme.com/api/v1/api-registry/ahfv4g1mj46g57s
- **API base URL:** `https://api.smartreach.io/api/v3`

## Authentication

### API Key

Use a SmartReach user API key. SmartReach requires the API key in the X-API-KEY header. Team-scoped endpoints also require a team_id query parameter during action runs.

### Credentials

- **API Key:** `apiKey` · required
- **Team ID:** `teamId` · required · SmartReach team identifier for this connection. It is used to populate the required team_id query parameter on team-scoped API requests.

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://help.smartreach.io/reference/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |
| `content-type` | `application/json` |

Responses from this API use JSON.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Domains to Do Not Contact List](actions/add-domains-to-do-not-contact-list.md) | `POST /do_not_contact/domain` | [docs](https://help.smartreach.io/reference/adddomainstodnc) |
| [Add Emails to Do Not Contact List](actions/add-emails-to-do-not-contact-list.md) | `POST /do_not_contact/email` | [docs](https://help.smartreach.io/reference/addemailstodnc) |
| [Add or Update Prospects](actions/add-or-update-prospects.md) | `POST /prospects` | [docs](https://help.smartreach.io/reference/addprospects) |
| [Add Prospects To Campaign](actions/add-prospects-to-campaign.md) | `POST /campaigns/:campaign_id/prospects` | [docs](https://help.smartreach.io/reference/post_campaigns-campaign-id-prospects) |
| [Create or Update Account](actions/create-or-update-account.md) | `POST /accounts` | [docs](https://help.smartreach.io/reference/post_accounts) |
| [Get Account](actions/get-account.md) | `GET /accounts/:account_id` | [docs](https://help.smartreach.io/reference/get_accounts-account-id) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:campaign_id` | [docs](https://help.smartreach.io/reference/getcampaign) |
| [Get Campaign Channel Settings](actions/get-campaign-channel-settings.md) | `GET /campaigns/:campaign_id/channel_settings` | [docs](https://help.smartreach.io/reference/channelsettings) |
| [Get Campaign Stats](actions/get-campaign-stats.md) | `GET /campaigns/:campaign_id/stats` | [docs](https://help.smartreach.io/reference/getcampaignstats) |
| [Get Email Setting](actions/get-email-setting.md) | `GET /email_settings/:email_setting_id` | [docs](https://help.smartreach.io/reference/get_email-settings-email-setting-id) |
| [Get Team](actions/get-team.md) | `GET /teams/:team_id` | [docs](https://help.smartreach.io/reference/getteambyid) |
| [Get User](actions/get-user.md) | `GET /user/:userId` | [docs](https://help.smartreach.io/reference/getuserbyid) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://help.smartreach.io/reference/accounts) |
| [List Campaign Prospects](actions/list-campaign-prospects.md) | `GET /campaigns/:campaign_id/prospects` | [docs](https://help.smartreach.io/reference/get_campaigns-campaign-id-prospects) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://help.smartreach.io/reference/getcampaigns) |
| [List Do Not Contact List](actions/list-do-not-contact-list.md) | `GET /do_not_contact` | [docs](https://help.smartreach.io/reference/getdnc) |
| [List Email Settings](actions/list-email-settings.md) | `GET /email_settings` | [docs](https://help.smartreach.io/reference/get_email-settings) |
| [List Prospects](actions/list-prospects.md) | `GET /prospects` | [docs](https://help.smartreach.io/reference/getprospects) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://help.smartreach.io/reference/getteams) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://help.smartreach.io/reference/getusers) |
| [Remove Do Not Contact Entries](actions/remove-do-not-contact-entries.md) | `DELETE /do_not_contact` | [docs](https://help.smartreach.io/reference/deletednc) |
| [Remove Prospects From Campaign](actions/remove-prospects-from-campaign.md) | `PUT /campaigns/:campaign_id/prospects` | [docs](https://help.smartreach.io/reference/put_campaigns-campaign-id-prospects) |
| [Update Campaign Status](actions/update-campaign-status.md) | `PUT /campaigns/:campaign_id/status` | [docs](https://help.smartreach.io/reference/startstopcampaign) |
| [Update Prospect Status](actions/update-prospect-status.md) | `PUT /prospects/prospect_status_change` | [docs](https://help.smartreach.io/reference/put_prospects-prospect-status-change) |
| [Update Task Status](actions/update-task-status.md) | `PUT /tasks/:task_id/status` | [docs](https://help.smartreach.io/reference/changetaskstatus) |
