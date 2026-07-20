# <img src="https://images.mindcloud.co/apps/icons/dubsado_1773080251531.png" alt="Dubsado logo" width="28" height="28"> Dubsado: Universal API

Manage clients, projects, forms, and invoices

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dubsado/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dubsado.com
- **Vendor API docs:** https://help.dubsado.com/en/articles/909872-connecting-with-zapier

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Zapier API Key](actions/validate-zapier-api-key.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dubsado/latest/actions/validate-zapier-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Appointments

| Action | Method | Description |
| --- | --- | --- |
| [List Calendar Appointments (Session Required)](actions/list-calendar-appointments-session-required.md) | GET |  |

### Calendars

| Action | Method | Description |
| --- | --- | --- |
| [List Calendars (Session Required)](actions/list-calendars-session-required.md) | GET |  |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [List Forms (Session Required)](actions/list-forms-session-required.md) | GET |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [List Calendar Projects (Session Required)](actions/list-calendar-projects-session-required.md) | GET |  |
| [List Projects (Session Required)](actions/list-projects-session-required.md) | GET |  |

### Scheduler

| Action | Method | Description |
| --- | --- | --- |
| [List Scheduler Dropdown Options (Session Required)](actions/list-scheduler-dropdown-options-session-required.md) | GET |  |
| [List Schedulers (Session Required)](actions/list-schedulers-session-required.md) | GET |  |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Lead Status Funnel Leads (Session Required)](actions/list-lead-status-funnel-leads-session-required.md) | GET |  |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Form Templates (Session Required)](actions/list-form-templates-session-required.md) | GET |  |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [List Workflow Templates (Session Required)](actions/list-workflow-templates-session-required.md) | GET |  |

### Zapier Key

| Action | Method | Description |
| --- | --- | --- |
| [Validate Zapier API Key](actions/validate-zapier-api-key.md) | GET | Validates a Zapier API key in Dubsado. |

