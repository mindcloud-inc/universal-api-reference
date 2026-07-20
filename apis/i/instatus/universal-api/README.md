# <img src="https://images.mindcloud.co/apps/icons/instatus-icon_1778103576030.png" alt="Instatus logo" width="28" height="28"> Instatus: Universal API

Instatus is an uptime monitoring, incident response, status page, and subscriber communication platform for managing service status, incidents, maintenances, components, subscribers, and monitoring workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/instatus/latest
- **Category:** IT Operations / Observability
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://instatus.com
- **Vendor API docs:** https://instatus.com/help/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Profile](actions/get-user-profile.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instatus/latest/actions/get-user-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Component

| Action | Method | Description |
| --- | --- | --- |
| [Create Component](actions/create-component.md) | POST |  |
| [Delete Component](actions/delete-component.md) | DELETE |  |
| [Get Component](actions/get-component.md) | GET |  |
| [List Components](actions/list-components.md) | GET |  |
| [Update Component](actions/update-component.md) | PUT |  |

### Incident

| Action | Method | Description |
| --- | --- | --- |
| [Create Incident](actions/create-incident.md) | POST |  |
| [Delete Incident](actions/delete-incident.md) | DELETE |  |
| [Get Incident](actions/get-incident.md) | GET |  |
| [List Incidents](actions/list-incidents.md) | GET |  |
| [Update Incident](actions/update-incident.md) | PUT |  |

### Incident Update

| Action | Method | Description |
| --- | --- | --- |
| [Create Incident Update](actions/create-incident-update.md) | POST |  |
| [Get Incident Update](actions/get-incident-update.md) | GET |  |
| [Update Incident Update](actions/update-incident-update.md) | PUT |  |

### Maintenance

| Action | Method | Description |
| --- | --- | --- |
| [Create Maintenance](actions/create-maintenance.md) | POST |  |
| [Delete Maintenance](actions/delete-maintenance.md) | DELETE |  |
| [Get Maintenance](actions/get-maintenance.md) | GET |  |
| [List Maintenances](actions/list-maintenances.md) | GET |  |
| [Update Maintenance](actions/update-maintenance.md) | PUT |  |

### Status Page

| Action | Method | Description |
| --- | --- | --- |
| [Create Status Page](actions/create-status-page.md) | POST |  |
| [Delete Status Page](actions/delete-status-page.md) | DELETE |  |
| [List Status Pages](actions/list-status-pages.md) | GET |  |
| [Update Status Page](actions/update-status-page.md) | PUT |  |

### Subscriber

| Action | Method | Description |
| --- | --- | --- |
| [List Subscribers](actions/list-subscribers.md) | GET |  |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get User Profile](actions/get-user-profile.md) | GET |  |

