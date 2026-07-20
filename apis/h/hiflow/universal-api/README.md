# <img src="https://images.mindcloud.co/apps/icons/hiflow_1776079445577.png" alt="Hiflow logo" width="28" height="28"> Hiflow: Universal API

Manage customers, projects, tasks, timesheets, estimates, and invoices

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hiflow/latest
- **Category:** Productivity / Project Management
- **Actions:** 2
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hiflow.net
- **Vendor API docs:** https://www.hiflow.net/openapi/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hiflow/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (2)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from Hiflow. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Hiflow. |

