# <img src="https://images.mindcloud.co/apps/icons/instantly_1777312158173.png" alt="Instantly logo" width="28" height="28"> Instantly: Universal API

Manage outreach campaigns, leads, accounts, and workspace settings

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/instantly/latest
- **Category:** Marketing
- **Actions:** 48
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://instantly.ai
- **Vendor API docs:** https://developer.instantly.ai

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Workspace](actions/get-current-workspace.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/get-current-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (48)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates a new account in Instantly. |
| [Get Account](actions/get-account.md) | GET | Retrieves an account from Instantly. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves accounts from Instantly. |
| [Pause Account](actions/pause-account.md) | PUT | Pauses an account in Instantly. |
| [Resume Account](actions/resume-account.md) | PUT | Resumes an account in Instantly. |
| [Update Account](actions/update-account.md) | PUT | Updates an existing account in Instantly. |

### Account Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Account Analytics](actions/get-daily-account-analytics.md) | GET | Retrieves daily account analytics from Instantly. |

### Account Vitals

| Action | Method | Description |
| --- | --- | --- |
| [Test Account Vitals](actions/test-account-vitals.md) | GET | Retrieves account vitals test results from Instantly. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Activate Campaign](actions/activate-campaign.md) | PUT | Activates a campaign in Instantly. |
| [Create Campaign](actions/create-campaign.md) | POST | Creates a new campaign in Instantly. |
| [Get Campaign](actions/get-campaign.md) | GET | Retrieves a campaign from Instantly. |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Instantly. |
| [Pause Campaign](actions/pause-campaign.md) | PUT | Pauses a campaign in Instantly. |
| [Search Campaigns By Contact](actions/search-campaigns-by-contact.md) | GET | Finds campaigns in Instantly by contact. |
| [Update Campaign](actions/update-campaign.md) | PUT | Updates an existing campaign in Instantly. |

### Campaign Analytics Overview

| Action | Method | Description |
| --- | --- | --- |
| [Get Campaign Analytics Overview](actions/get-campaign-analytics-overview.md) | GET | Retrieves campaign analytics overview from Instantly. |

### Daily Campaign Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Campaign Analytics](actions/get-daily-campaign-analytics.md) | GET | Retrieves daily campaign analytics from Instantly. |

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Delete Email](actions/delete-email.md) | DELETE | Deletes an email from Instantly. |
| [Forward Email](actions/forward-email.md) | POST | Forwards an email in Instantly. |
| [Get Email](actions/get-email.md) | GET | Retrieves an email from Instantly. |
| [Get Unread Email Count](actions/get-unread-email-count.md) | GET | Retrieves unread email counts from Instantly. |
| [List Emails](actions/list-emails.md) | GET | Retrieves emails from Instantly. |
| [Mark Email Thread As Read](actions/mark-email-thread-as-read.md) | PUT | Marks an email thread as read in Instantly. |
| [Reply To Email](actions/reply-to-email.md) | POST | Replies to an email in Instantly. |
| [Send Test Email](actions/send-test-email.md) | POST | Sends a test email from Instantly. |
| [Update Email](actions/update-email.md) | PUT | Updates an existing email in Instantly. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Add Leads To Campaign Or List](actions/add-leads-to-campaign-or-list.md) | POST | Adds leads to a campaign or list in Instantly. |
| [Bulk Assign Leads](actions/bulk-assign-leads.md) | PUT | Assigns leads to users in Instantly. |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in Instantly. |
| [Delete Lead](actions/delete-lead.md) | DELETE | Deletes an existing lead from Instantly. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from Instantly. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from Instantly. |
| [Merge Leads](actions/merge-leads.md) | PUT | Merges two leads in Instantly. |
| [Move Leads](actions/move-leads.md) | PUT | Moves leads to a campaign or list in Instantly. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in Instantly. |
| [Update Lead Interest Status](actions/update-lead-interest-status.md) | PUT | Updates a lead interest status in Instantly. |

### Lead List

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead List](actions/create-lead-list.md) | POST | Creates a new lead list in Instantly. |
| [Get Lead List](actions/get-lead-list.md) | GET | Retrieves a lead list from Instantly. |
| [List Lead Lists](actions/list-lead-lists.md) | GET | Retrieves lead lists from Instantly. |
| [Update Lead List](actions/update-lead-list.md) | PUT | Updates an existing lead list in Instantly. |

### Lead List Verification Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Lead List Verification Stats](actions/get-lead-list-verification-stats.md) | GET | Retrieves lead list verification stats from Instantly. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in Instantly. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from Instantly. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from Instantly. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Instantly. |
| [Resume Webhook](actions/resume-webhook.md) | PUT | Resumes a webhook in Instantly. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Instantly. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Workspace](actions/get-current-workspace.md) | GET | Retrieves the current workspace from Instantly. |

