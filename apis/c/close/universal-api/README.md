# <img src="https://images.mindcloud.co/apps/icons/close_1772651689350.png" alt="Close logo" width="28" height="28"> Close: Universal API

Manage leads, communicate across channels, automate follow-ups, and close deals.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/close/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://close.com
- **Vendor API docs:** https://developer.close.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/close/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | GET | Retrieves activities from Close. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Close. |
| [Delete Contact](actions/delete-contact.md) | DELETE | Deletes an existing contact from Close. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact from Close. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contacts from Close. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Close. |

### Email Template

| Action | Method | Description |
| --- | --- | --- |
| [Get Email Template](actions/get-email-template.md) | GET | Retrieves an email template from Close. |
| [List Email Templates](actions/list-email-templates.md) | GET | Retrieves email templates from Close. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in Close. |
| [Delete Lead](actions/delete-lead.md) | DELETE | Deletes an existing lead from Close. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead from Close. |
| [List Leads](actions/list-leads.md) | GET | Retrieves leads from Close. |
| [Merge Leads](actions/merge-leads.md) | POST | Merges two leads in Close. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in Close. |

### Lead Status

| Action | Method | Description |
| --- | --- | --- |
| [List Lead Statuses](actions/list-lead-statuses.md) | GET | Retrieves lead statuses from Close. |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity](actions/create-opportunity.md) | POST | Creates a new opportunity in Close. |
| [Delete Opportunity](actions/delete-opportunity.md) | DELETE | Deletes an existing opportunity from Close. |
| [Get Opportunity](actions/get-opportunity.md) | GET | Retrieves an opportunity from Close. |
| [List Opportunities](actions/list-opportunities.md) | GET | Retrieves opportunities from Close. |
| [Update Opportunity](actions/update-opportunity.md) | PUT | Updates an existing opportunity in Close. |

### Opportunity Status

| Action | Method | Description |
| --- | --- | --- |
| [List Opportunity Statuses](actions/list-opportunity-statuses.md) | GET | Retrieves opportunity statuses from Close. |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [List Pipelines](actions/list-pipelines.md) | GET | Retrieves pipelines from Close. |

### Sequence

| Action | Method | Description |
| --- | --- | --- |
| [List Sequences](actions/list-sequences.md) | GET | Retrieves workflow sequences from Close. |

### Smart View

| Action | Method | Description |
| --- | --- | --- |
| [Create Smart View](actions/create-smart-view.md) | POST | Creates a new smart view in Close. |
| [Delete Smart View](actions/delete-smart-view.md) | DELETE | Deletes an existing smart view from Close. |
| [Get Smart View](actions/get-smart-view.md) | GET | Retrieves a smart view from Close. |
| [List Smart Views](actions/list-smart-views.md) | GET | Retrieves smart views from Close. |
| [Update Smart View](actions/update-smart-view.md) | PUT | Updates an existing smart view in Close. |

### Sms Template

| Action | Method | Description |
| --- | --- | --- |
| [Get SMS Template](actions/get-sms-template.md) | GET | Retrieves an SMS template from Close. |
| [List SMS Templates](actions/list-sms-templates.md) | GET | Retrieves SMS templates from Close. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Close. |
| [Delete Task](actions/delete-task.md) | DELETE | Deletes an existing task from Close. |
| [Get Task](actions/get-task.md) | GET | Retrieves a task from Close. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Close. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Close. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves your current user profile from Close. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from Close. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Close. |

### User Availability

| Action | Method | Description |
| --- | --- | --- |
| [List User Availabilities](actions/list-user-availabilities.md) | GET | Retrieves user availability statuses from Close. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook subscription from Close. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhook subscriptions from Close. |

