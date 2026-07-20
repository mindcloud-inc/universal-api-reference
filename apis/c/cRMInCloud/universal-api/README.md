# <img src="https://images.mindcloud.co/apps/icons/favicon-app-crmincloud-it-48x48_1777381308427.png" alt="CRM in Cloud logo" width="28" height="28"> CRM in Cloud: Universal API

CRM in Cloud is TeamSystem's CRM platform for managing companies, contacts, leads, opportunities, activities, quotes, orders, and related sales workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cRMInCloud/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.teamsystem.com/store/crm-in-cloud/
- **Vendor API docs:** https://app.crmincloud.it/api/v1/Docs/Home

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Count activities](actions/count-activities.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cRMInCloud/latest/actions/count-activities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [Search activities](actions/search-activities.md) | GET | Finds activities in CRM in Cloud. |

### Activity Count

| Action | Method | Description |
| --- | --- | --- |
| [Count activities](actions/count-activities.md) | GET | Retrieves the number of activities in CRM in Cloud. |

### Activity Template

| Action | Method | Description |
| --- | --- | --- |
| [Get new activity instance](actions/get-new-activity-instance.md) | GET | Retrieves a new activity template from CRM in Cloud. |

### Appointment

| Action | Method | Description |
| --- | --- | --- |
| [Search appointments](actions/search-appointments.md) | GET | Finds appointments in CRM in Cloud. |

### Appointment Count

| Action | Method | Description |
| --- | --- | --- |
| [Count appointments](actions/count-appointments.md) | GET | Retrieves the number of appointments in CRM in Cloud. |

### Appointment Template

| Action | Method | Description |
| --- | --- | --- |
| [Get new appointment instance](actions/get-new-appointment-instance.md) | GET | Retrieves a new appointment template from CRM in Cloud. |

### Company

| Action | Method | Description |
| --- | --- | --- |
| [Search companies](actions/search-companies.md) | GET | Finds companies in CRM in Cloud. |

### Company Count

| Action | Method | Description |
| --- | --- | --- |
| [Count companies](actions/count-companies.md) | GET | Retrieves the number of companies in CRM in Cloud. |

### Company Template

| Action | Method | Description |
| --- | --- | --- |
| [Get new company instance](actions/get-new-company-instance.md) | GET | Retrieves a new company template from CRM in Cloud. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Search contacts](actions/search-contacts.md) | GET | Finds contacts in CRM in Cloud. |

### Contact Count

| Action | Method | Description |
| --- | --- | --- |
| [Count contacts](actions/count-contacts.md) | GET | Retrieves the number of contacts in CRM in Cloud. |

### Contact Template

| Action | Method | Description |
| --- | --- | --- |
| [Get new contact instance](actions/get-new-contact-instance.md) | GET | Retrieves a new contact template from CRM in Cloud. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Search leads](actions/search-leads.md) | GET | Finds leads in CRM in Cloud. |

### Lead Count

| Action | Method | Description |
| --- | --- | --- |
| [Count leads](actions/count-leads.md) | GET | Retrieves the number of leads in CRM in Cloud. |

### Lead Template

| Action | Method | Description |
| --- | --- | --- |
| [Get new lead instance](actions/get-new-lead-instance.md) | GET | Retrieves a new lead template from CRM in Cloud. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Search lists](actions/search-lists.md) | GET | Finds lists in CRM in Cloud. |

### List Count

| Action | Method | Description |
| --- | --- | --- |
| [Count lists](actions/count-lists.md) | GET | Retrieves the number of lists in CRM in Cloud. |

### List Template

| Action | Method | Description |
| --- | --- | --- |
| [Get new list instance](actions/get-new-list-instance.md) | GET | Retrieves a new list template from CRM in Cloud. |

### Opportunity

| Action | Method | Description |
| --- | --- | --- |
| [Search opportunities](actions/search-opportunities.md) | GET | Finds opportunities in CRM in Cloud. |

### Opportunity Count

| Action | Method | Description |
| --- | --- | --- |
| [Count opportunities](actions/count-opportunities.md) | GET | Retrieves the number of opportunities in CRM in Cloud. |

### Opportunity Template

| Action | Method | Description |
| --- | --- | --- |
| [Get new opportunity instance](actions/get-new-opportunity-instance.md) | GET | Retrieves a new opportunity template from CRM in Cloud. |

### Storage Item

| Action | Method | Description |
| --- | --- | --- |
| [Search storage items](actions/search-storage-items.md) | GET | Finds storage items in CRM in Cloud. |

### Storage Item Count

| Action | Method | Description |
| --- | --- | --- |
| [Count storage items](actions/count-storage-items.md) | GET | Retrieves the number of storage items in CRM in Cloud. |

### Storage Item Template

| Action | Method | Description |
| --- | --- | --- |
| [Get new storage item instance](actions/get-new-storage-item-instance.md) | GET | Retrieves a new storage item template from CRM in Cloud. |

