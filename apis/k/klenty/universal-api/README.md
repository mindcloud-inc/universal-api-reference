# <img src="https://images.mindcloud.co/apps/icons/klenty_1774296439721.png" alt="Klenty logo" width="28" height="28"> Klenty: Universal API

Manage prospects, lists, cadences, and sales outreach

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/klenty/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.klenty.com
- **Vendor API docs:** https://support.klenty.com/en/collections/5599717-webhooks-apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Lists](actions/list-lists.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klenty/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Cadence

| Action | Method | Description |
| --- | --- | --- |
| [List Company Cadences](actions/list-company-cadences.md) | GET | Retrieves company cadences from Klenty. |
| [List User Cadences](actions/list-user-cadences.md) | GET | Retrieves user cadences from Klenty. |
| [Start Cadence](actions/start-cadence.md) | POST | Starts a cadence in Klenty. |

### Call

| Action | Method | Description |
| --- | --- | --- |
| [Get Call Completion Details](actions/get-call-completion-details.md) | GET | Retrieves call completion details from Klenty. |

### Email Engagement

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Engagements](actions/get-email-engagements.md) | GET | Retrieves email engagements from Klenty. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [List Lists](actions/list-lists.md) | GET | Retrieves lists from Klenty. |

### Prospect

| Action | Method | Description |
| --- | --- | --- |
| [Add Prospect Custom Field Value](actions/add-prospect-custom-field-value.md) | PUT | Adds a custom field value to a prospect in Klenty. |
| [Add Prospect To List](actions/add-prospect-to-list.md) | PUT | Adds a prospect to a list in Klenty. |
| [Add Tags To Prospect](actions/add-tags-to-prospect.md) | PUT | Adds tags to a prospect in Klenty. |
| [Bulk Create Prospects](actions/bulk-create-prospects.md) | POST | Creates prospects in bulk in Klenty. |
| [Change Prospect To Do Not Contact](actions/change-prospect-to-do-not-contact.md) | PUT | Changes a prospect to do not contact in Klenty. |
| [Create Prospect](actions/create-prospect.md) | POST | Creates a prospect in Klenty. |
| [Get Prospect By Email](actions/get-prospect-by-email.md) | GET | Retrieves a prospect from Klenty by email. |
| [Get Prospect Status By Email](actions/get-prospect-status-by-email.md) | GET | Retrieves prospect status from Klenty by email. |
| [Get Prospect Status By ID](actions/get-prospect-status-by-id.md) | GET | Retrieves prospect status from Klenty by ID. |
| [Get Prospect With Custom Fields](actions/get-prospect-with-custom-fields.md) | GET | Retrieves a prospect with custom fields from Klenty. |
| [List Prospects By Created Date](actions/list-prospects-by-created-date.md) | GET | Retrieves prospects from Klenty by created date. |
| [List Prospects By Last Updated Date](actions/list-prospects-by-last-updated-date.md) | GET | Retrieves prospects from Klenty by last updated date. |
| [List Prospects By List](actions/list-prospects-by-list.md) | GET | Retrieves prospects from a Klenty list. |
| [Remove Tags From Prospect](actions/remove-tags-from-prospect.md) | PUT | Removes tags from a prospect in Klenty. |
| [Resume Cadence](actions/resume-cadence.md) | PUT | Resumes cadence for a prospect in Klenty. |
| [Revert Prospect From Do Not Contact](actions/revert-prospect-from-do-not-contact.md) | PUT | Reverts a prospect from do not contact in Klenty. |
| [Stop Cadence For Prospect](actions/stop-cadence-for-prospect.md) | PUT | Stops cadence for a prospect in Klenty. |
| [Stop Prospect Mails](actions/stop-prospect-mails.md) | PUT | Stops mails for a prospect in Klenty. |
| [Unsubscribe Prospect](actions/unsubscribe-prospect.md) | PUT | Unsubscribes a prospect in Klenty. |
| [Update Prospect](actions/update-prospect.md) | PUT | Updates an existing prospect in Klenty. |

### Stepwise Metric Engagement

| Action | Method | Description |
| --- | --- | --- |
| [Get Stepwise Metric Engagements](actions/get-stepwise-metric-engagements.md) | GET | Retrieves stepwise metric engagements from Klenty. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Add Webhook](actions/add-webhook.md) | POST | Creates a webhook in Klenty. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes an existing webhook from Klenty. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from Klenty. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in Klenty. |

