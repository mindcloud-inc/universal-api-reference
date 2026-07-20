# <img src="https://images.mindcloud.co/apps/icons/image-09b86b2bf0_1776104805195.png" alt="Vacation Tracker logo" width="28" height="28"> Vacation Tracker: Universal API

Manage PTO users, leaves, locations, and leave types

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vacationTracker/latest
- **Category:** Human Resources / HRIS
- **Actions:** 6
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vacationtracker.io
- **Vendor API docs:** https://vacationtracker.io/developers/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Departments](actions/list-departments.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vacationTracker/latest/actions/list-departments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (6)

### Employees

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET |  |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Departments](actions/list-departments.md) | GET |  |

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [List Labels](actions/list-labels.md) | GET |  |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [List Locations](actions/list-locations.md) | GET |  |

### Time Off

| Action | Method | Description |
| --- | --- | --- |
| [List Leave Types](actions/list-leave-types.md) | GET |  |
| [List Leaves](actions/list-leaves.md) | GET |  |

