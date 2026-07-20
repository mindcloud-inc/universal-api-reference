# Instantly: Native API Reference

A consolidated summary of Instantly's API configuration and 48 documented operations, with links to official documentation.

- **Official docs:** https://developer.instantly.ai
- **API base URL:** `https://api.instantly.ai`

## Authentication

### API Key

Authenticate with an Instantly API V2 bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.instantly.ai)

## API conventions

Responses from this API use JSON. The next-page cursor is read from `next_starting_after`.

## Pagination

Use `limit` in the query string to set the page size (default 10; accepted range 1–100). Use `starting_after` in the query string as the pagination cursor.

## Filtering

Send filters in the query string. Supported operators: `eq`, `like`.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (48 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Campaign](actions/activate-campaign.md) | `POST /api/v2/campaigns/:id/activate` | [docs](https://developer.instantly.ai/api/v2/campaign/activatecampaign) |
| [Add Leads To Campaign Or List](actions/add-leads-to-campaign-or-list.md) | `POST /api/v2/leads/add` | [docs](https://developer.instantly.ai/api-reference/lead/add-leads-in-bulk-to-a-campaign-or-list) |
| [Bulk Assign Leads](actions/bulk-assign-leads.md) | `POST /api/v2/leads/bulk-assign` | [docs](https://developer.instantly.ai/api-reference/lead/bulk-assign-leads-to-organization-users) |
| [Create Account](actions/create-account.md) | `POST /api/v2/accounts` | [docs](https://developer.instantly.ai/api/v2/account/createaccount) |
| [Create Campaign](actions/create-campaign.md) | `POST /api/v2/campaigns` | [docs](https://developer.instantly.ai/api/v2/campaign/createcampaign) |
| [Create Lead](actions/create-lead.md) | `POST /api/v2/leads` | [docs](https://developer.instantly.ai/api-reference/lead/create-lead) |
| [Create Lead List](actions/create-lead-list.md) | `POST /api/v2/lead-lists` | [docs](https://developer.instantly.ai/api-reference/leadlist/create-lead-list) |
| [Create Webhook](actions/create-webhook.md) | `POST /api/v2/webhooks` | [docs](https://developer.instantly.ai/api/v2/webhook/createwebhook) |
| [Delete Email](actions/delete-email.md) | `DELETE /api/v2/emails/:id` | [docs](https://developer.instantly.ai/api/v2/email/deleteemail) |
| [Delete Lead](actions/delete-lead.md) | `DELETE /api/v2/leads/:id` | [docs](https://developer.instantly.ai/api-reference/lead/delete-lead) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /api/v2/webhooks/:id` | [docs](https://developer.instantly.ai/api-reference/webhook/delete-webhook) |
| [Forward Email](actions/forward-email.md) | `POST /api/v2/emails/forward` | [docs](https://developer.instantly.ai/api-reference/email/forward-an-email) |
| [Get Account](actions/get-account.md) | `GET /api/v2/accounts/:email` | [docs](https://developer.instantly.ai/api/v2/account/getaccount) |
| [Get Campaign](actions/get-campaign.md) | `GET /api/v2/campaigns/:id` | [docs](https://developer.instantly.ai/api/v2/campaign/getcampaign) |
| [Get Campaign Analytics Overview](actions/get-campaign-analytics-overview.md) | `GET /api/v2/campaigns/analytics/overview` | [docs](https://developer.instantly.ai/api/v2/campaign/getcampaignanalyticsoverview) |
| [Get Current Workspace](actions/get-current-workspace.md) | `GET /api/v2/workspaces/current` | [docs](https://developer.instantly.ai/api/v2/workspace) |
| [Get Daily Account Analytics](actions/get-daily-account-analytics.md) | `GET /api/v2/accounts/analytics/daily` | [docs](https://developer.instantly.ai/api/v2/account/getdailyaccountanalytics) |
| [Get Daily Campaign Analytics](actions/get-daily-campaign-analytics.md) | `GET /api/v2/campaigns/analytics/daily` | [docs](https://developer.instantly.ai/api/v2/campaign/getdailycampaignanalytics) |
| [Get Email](actions/get-email.md) | `GET /api/v2/emails/:id` | [docs](https://developer.instantly.ai/api-reference/email/get-email) |
| [Get Lead](actions/get-lead.md) | `GET /api/v2/leads/:id` | [docs](https://developer.instantly.ai/api-reference/lead/get-lead) |
| [Get Lead List](actions/get-lead-list.md) | `GET /api/v2/lead-lists/:id` | [docs](https://developer.instantly.ai/api/v2/leadlist) |
| [Get Lead List Verification Stats](actions/get-lead-list-verification-stats.md) | `GET /api/v2/lead-lists/:id/verification-stats` | [docs](https://developer.instantly.ai/api/v2/leadlist) |
| [Get Unread Email Count](actions/get-unread-email-count.md) | `GET /api/v2/emails/unread/count` | [docs](https://developer.instantly.ai/api/v2/email/countunreademails) |
| [Get Webhook](actions/get-webhook.md) | `GET /api/v2/webhooks/:id` | [docs](https://developer.instantly.ai/api-reference/webhook/get-webhook) |
| [List Accounts](actions/list-accounts.md) | `GET /api/v2/accounts` | [docs](https://developer.instantly.ai/api/v2/account/listaccount) |
| [List Campaigns](actions/list-campaigns.md) | `GET /api/v2/campaigns` | [docs](https://developer.instantly.ai/api/v2/campaign/listcampaign) |
| [List Emails](actions/list-emails.md) | `GET /api/v2/emails` | [docs](https://developer.instantly.ai/api/v2/email/listemails) |
| [List Lead Lists](actions/list-lead-lists.md) | `GET /api/v2/lead-lists` | [docs](https://developer.instantly.ai/api/v2/leadlist) |
| [List Leads](actions/list-leads.md) | `POST /api/v2/leads/list` | [docs](https://developer.instantly.ai/api-reference/lead/list-leads) |
| [List Webhooks](actions/list-webhooks.md) | `GET /api/v2/webhooks` | [docs](https://developer.instantly.ai/api/v2/webhook/listwebhooks) |
| [Mark Email Thread As Read](actions/mark-email-thread-as-read.md) | `POST /api/v2/emails/threads/:thread_id/mark-as-read` | [docs](https://developer.instantly.ai/api/v2/email/markallemailsinathreadasread) |
| [Merge Leads](actions/merge-leads.md) | `POST /api/v2/leads/merge` | [docs](https://developer.instantly.ai/api-reference/lead/merge-two-leads) |
| [Move Leads](actions/move-leads.md) | `POST /api/v2/leads/move` | [docs](https://developer.instantly.ai/api-reference/lead/move-leads-to-a-campaign-or-list) |
| [Pause Account](actions/pause-account.md) | `POST /api/v2/accounts/:email/pause` | [docs](https://developer.instantly.ai/api/v2/account/pauseaccount) |
| [Pause Campaign](actions/pause-campaign.md) | `POST /api/v2/campaigns/:id/pause` | [docs](https://developer.instantly.ai/api/v2/campaign/pausecampaign) |
| [Reply To Email](actions/reply-to-email.md) | `POST /api/v2/emails/reply` | [docs](https://developer.instantly.ai/api-reference/email/reply-to-an-email) |
| [Resume Account](actions/resume-account.md) | `POST /api/v2/accounts/:email/resume` | [docs](https://developer.instantly.ai/api/v2/account/resumeaccount) |
| [Resume Webhook](actions/resume-webhook.md) | `POST /api/v2/webhooks/:id/resume` | [docs](https://developer.instantly.ai/api-reference/webhook/resume-a-webhook) |
| [Search Campaigns By Contact](actions/search-campaigns-by-contact.md) | `GET /api/v2/campaigns/search-by-contact` | [docs](https://developer.instantly.ai/api/v2/campaign/searchbycontact) |
| [Send Test Email](actions/send-test-email.md) | `POST /api/v2/emails/test` | [docs](https://developer.instantly.ai/api/v2/email/sendtestemail) |
| [Test Account Vitals](actions/test-account-vitals.md) | `POST /api/v2/accounts/test/vitals` | [docs](https://developer.instantly.ai/api/v2/account/testaccountvitals) |
| [Update Account](actions/update-account.md) | `PATCH /api/v2/accounts/:email` | [docs](https://developer.instantly.ai/api/v2/account/patchaccount) |
| [Update Campaign](actions/update-campaign.md) | `PATCH /api/v2/campaigns/:id` | [docs](https://developer.instantly.ai/api/v2/campaign/patchcampaign) |
| [Update Email](actions/update-email.md) | `PATCH /api/v2/emails/:id` | [docs](https://developer.instantly.ai/api/v2/email/patchemail) |
| [Update Lead](actions/update-lead.md) | `PATCH /api/v2/leads/:id` | [docs](https://developer.instantly.ai/api-reference/lead/patch-lead) |
| [Update Lead Interest Status](actions/update-lead-interest-status.md) | `POST /api/v2/leads/update-interest-status` | [docs](https://developer.instantly.ai/api-reference/lead/update-the-interest-status-of-a-lead) |
| [Update Lead List](actions/update-lead-list.md) | `PATCH /api/v2/lead-lists/:id` | [docs](https://developer.instantly.ai/api/v2/leadlist) |
| [Update Webhook](actions/update-webhook.md) | `PATCH /api/v2/webhooks/:id` | [docs](https://developer.instantly.ai/api/v2/webhook/patchwebhook) |
