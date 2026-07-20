# lemlist: Native API Reference

A consolidated summary of lemlist's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://developer.lemlist.com/api-reference/getting-started/overview
- **API base URL:** `https://api.lemlist.com/api`

## Authentication

### API Key

Authenticate with your lemlist API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.lemlist.com/api-reference/introduction/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `offset` in the query string as the record offset.

## Sorting

Set the sort field with `sortBy` in the query string. Set the direction separately with `sortOrder`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Webhook](actions/add-webhook.md) | `POST /hooks` | [docs](https://developer.lemlist.com/api-reference/endpoints/webhooks/add-webhook) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaigns` | [docs](https://developer.lemlist.com/api-reference/endpoints/campaigns/create-campaign) |
| [Create Lead in Campaign](actions/create-lead-in-campaign.md) | `POST /campaigns/:campaignId/leads/` | [docs](https://developer.lemlist.com/api-reference/endpoints/leads/create-lead-in-campaign) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:campaignId` | [docs](https://developer.lemlist.com/api-reference/endpoints/campaigns/get-campaign) |
| [Get Campaign Stats](actions/get-campaign-stats.md) | `GET /v2/campaigns/:campaignId/stats` | [docs](https://developer.lemlist.com/api-reference/endpoints/campaigns/get-campaign-stats) |
| [Get Lead by Email](actions/get-lead-by-email.md) | `GET /leads/:email` | [docs](https://developer.lemlist.com/api-reference/endpoints/leads/get-lead-by-email) |
| [Get Team Credits](actions/get-team-credits.md) | `GET /team/credits` | [docs](https://developer.lemlist.com/api-reference/endpoints/team/get-team-credits) |
| [List Activities](actions/list-activities.md) | `GET /activities` | [docs](https://developer.lemlist.com/api-reference/endpoints/activities/get-many-activities) |
| [List Campaign Leads](actions/list-campaign-leads.md) | `GET /campaigns/:campaignId/leads/` | [docs](https://developer.lemlist.com/api-reference/endpoints/leads/get-campaign-leads) |
| [List Campaign Sequences](actions/list-campaign-sequences.md) | `GET /campaigns/:campaignId/sequences` | [docs](https://developer.lemlist.com/api-reference/endpoints/sequences/get-campaign-sequences) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://developer.lemlist.com/api-reference/endpoints/campaigns/get-many-campaigns) |
| [List Contact Messages](actions/list-contact-messages.md) | `GET /inbox/:contactId` | [docs](https://developer.lemlist.com/api-reference/endpoints/inbox/get-contact-messages) |
| [List Inboxes](actions/list-inboxes.md) | `GET /inbox` | [docs](https://developer.lemlist.com/api-reference/endpoints/inbox/get-many-inboxes) |
| [Mark Lead as Interested in Campaign](actions/mark-lead-as-interested-in-campaign.md) | `POST /campaigns/:campaignId/leads/:leadIdOrEmail/interested` | [docs](https://developer.lemlist.com/api-reference/endpoints/leads/mark-lead-as-interested-in-campaign) |
| [Mark Lead as Not Interested in Campaign](actions/mark-lead-as-not-interested-in-campaign.md) | `POST /campaigns/:campaignId/leads/:leadIdOrEmail/notinterested` | [docs](https://developer.lemlist.com/api-reference/endpoints/leads/mark-lead-as-not-interested-in-campaign) |
| [Pause Campaign](actions/pause-campaign.md) | `POST /campaigns/:campaignId/pause` | [docs](https://developer.lemlist.com/api-reference/endpoints/campaigns/pause-campaign) |
| [Pause Lead](actions/pause-lead.md) | `POST /leads/pause/:leadId` | [docs](https://developer.lemlist.com/api-reference/endpoints/leads/pause-lead) |
| [Resume Paused Lead](actions/resume-paused-lead.md) | `POST /leads/start/:leadId` | [docs](https://developer.lemlist.com/api-reference/endpoints/leads/resume-paused-lead) |
| [Send Email](actions/send-email.md) | `POST /inbox/email` | [docs](https://developer.lemlist.com/api-reference/endpoints/inbox/send-email) |
| [Start Campaign](actions/start-campaign.md) | `POST /campaigns/:campaignId/start` | [docs](https://developer.lemlist.com/api-reference/endpoints/campaigns/start-campaign) |
| [Update Campaign](actions/update-campaign.md) | `PATCH /campaigns/:campaignId` | [docs](https://developer.lemlist.com/api-reference/endpoints/campaigns/update-campaign) |
| [Update Lead in a Campaign](actions/update-lead-in-a-campaign.md) | `PATCH /campaigns/:campaignId/leads/:leadId` | [docs](https://developer.lemlist.com/api-reference/endpoints/leads/update-lead) |
