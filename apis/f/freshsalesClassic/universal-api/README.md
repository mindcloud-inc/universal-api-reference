# <img src="https://images.mindcloud.co/apps/icons/freshsales-classic-512x520_1773870996882.png" alt="Freshsales Classic logo" width="28" height="28"> Freshsales Classic: Universal API

Freshsales Classic is a Freshworks CRM integration for managing contacts, accounts, deals, tasks, search, and related sales data through the legacy Freshsales API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/freshsalesClassic/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 29
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://support.freshsales.io/
- **Vendor API docs:** https://developers.freshworks.com/crm/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Owners](actions/list-owners.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-owners?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (29)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [List All Account Fields](actions/list-all-account-fields.md) | GET | Retrieves account fields from Freshsales Classic. |
| [List All Accounts](actions/list-all-accounts.md) | GET | Retrieves accounts from a Freshsales Classic view. |
| [View an Account](actions/view-an-account.md) | GET | Retrieves an account from Freshsales Classic. |

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Contact Activities](actions/list-contact-activities.md) | GET | Retrieves activities for a contact from Freshsales Classic. |

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [List All Appointments](actions/list-all-appointments.md) | GET | Retrieves appointments from Freshsales Classic. |
| [View an Appointment](actions/view-an-appointment.md) | GET | Retrieves an appointment from Freshsales Classic. |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [List Campaigns](actions/list-campaigns.md) | GET | Retrieves campaigns from Freshsales Classic. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [List All Contact Fields](actions/list-all-contact-fields.md) | GET | Retrieves contact fields from Freshsales Classic. |
| [List All Contacts](actions/list-all-contacts.md) | GET | Retrieves contacts from a Freshsales Classic view. |
| [List Contact Statuses](actions/list-contact-statuses.md) | GET | Retrieves contact statuses from Freshsales Classic. |
| [View a Contact](actions/view-a-contact.md) | GET | Retrieves a contact from Freshsales Classic. |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [List All Deal Fields](actions/list-all-deal-fields.md) | GET | Retrieves deal fields from Freshsales Classic. |
| [List All Deals](actions/list-all-deals.md) | GET | Retrieves deals from a Freshsales Classic view. |
| [View a Deal](actions/view-a-deal.md) | GET | Retrieves a deal from Freshsales Classic. |

### Deal Stage

| Action | Method | Description |
| --- | --- | --- |
| [List Deal Stages](actions/list-deal-stages.md) | GET | Retrieves deal stages from Freshsales Classic. |

### Engagements

| Action | Method | Description |
| --- | --- | --- |
| [List Sales Activity Types](actions/list-sales-activity-types.md) | GET | Retrieves sales activity types from Freshsales Classic. |

### Lifecycle

| Action | Method | Description |
| --- | --- | --- |
| [List Lifecycle Stages](actions/list-lifecycle-stages.md) | GET | Retrieves lifecycle stages from Freshsales Classic. |

### Pipeline

| Action | Method | Description |
| --- | --- | --- |
| [List Deal Pipelines](actions/list-deal-pipelines.md) | GET | Retrieves deal pipelines from Freshsales Classic. |

### Sales Activity

| Action | Method | Description |
| --- | --- | --- |
| [List All Sales Activities](actions/list-all-sales-activities.md) | GET | Retrieves sales activities from Freshsales Classic. |
| [List All Sales Activity Fields](actions/list-all-sales-activity-fields.md) | GET | Retrieves sales activity fields from Freshsales Classic. |
| [View a Sales Activity](actions/view-a-sales-activity.md) | GET | Retrieves a sales activity from Freshsales Classic. |

### Search

| Action | Method | Description |
| --- | --- | --- |
| [Lookup Search](actions/lookup-search.md) | GET | Finds lookup records in Freshsales Classic by query. |
| [Search](actions/search.md) | GET | Finds records in Freshsales Classic by query. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [List All Tasks](actions/list-all-tasks.md) | GET | Retrieves tasks from Freshsales Classic. |
| [View a Task](actions/view-a-task.md) | GET | Retrieves a task from Freshsales Classic. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Owners](actions/list-owners.md) | GET | Retrieves owners from Freshsales Classic. |

### View

| Action | Method | Description |
| --- | --- | --- |
| [List Account Views](actions/list-account-views.md) | GET | Retrieves account views from Freshsales Classic. |
| [List Contact Views](actions/list-contact-views.md) | GET | Retrieves contact views from Freshsales Classic. |
| [List Deal Views](actions/list-deal-views.md) | GET | Retrieves deal views from Freshsales Classic. |

