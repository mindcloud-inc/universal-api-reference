# <img src="https://images.mindcloud.co/apps/icons/pingdom_1774471428511.png" alt="Pingdom logo" width="28" height="28"> Pingdom: Universal API

Monitor uptime, manage alerts, and run synthetic checks

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pingdom/latest
- **Category:** IT Operations / Observability
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pingdom.com
- **Vendor API docs:** https://docs.pingdom.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Credits](actions/get-credits.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/get-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Alerts

| Action | Method | Description |
| --- | --- | --- |
| [List Actions](actions/list-actions.md) | GET |  |

### Check Result

| Action | Method | Description |
| --- | --- | --- |
| [List Check Results](actions/list-check-results.md) | GET |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST |  |
| [Delete Contact](actions/delete-contact.md) | DELETE |  |
| [Get Contact](actions/get-contact.md) | GET |  |
| [List Contacts](actions/list-contacts.md) | GET |  |
| [Update Contact](actions/update-contact.md) | PUT |  |

### Credits

| Action | Method | Description |
| --- | --- | --- |
| [Get Credits](actions/get-credits.md) | GET |  |

### Maintenance Window

| Action | Method | Description |
| --- | --- | --- |
| [Create Maintenance Window](actions/create-maintenance-window.md) | POST |  |
| [Delete Maintenance Window](actions/delete-maintenance-window.md) | DELETE |  |
| [Get Maintenance Window](actions/get-maintenance-window.md) | GET |  |
| [List Maintenance Windows](actions/list-maintenance-windows.md) | GET |  |
| [Update Maintenance Window](actions/update-maintenance-window.md) | PUT |  |

### Monitors

| Action | Method | Description |
| --- | --- | --- |
| [Create Check](actions/create-check.md) | POST |  |
| [Delete Check](actions/delete-check.md) | DELETE |  |
| [Get Check](actions/get-check.md) | GET |  |
| [List Checks](actions/list-checks.md) | GET |  |
| [Update Check](actions/update-check.md) | PUT |  |
| [Update Checks](actions/update-checks.md) | PUT |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [Create Team](actions/create-team.md) | POST |  |
| [Delete Team](actions/delete-team.md) | DELETE |  |
| [Get Team](actions/get-team.md) | GET |  |
| [List Teams](actions/list-teams.md) | GET |  |
| [Update Team](actions/update-team.md) | PUT |  |

