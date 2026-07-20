# <img src="https://images.mindcloud.co/apps/icons/7-time_1775589174468.png" alt="Seven Time logo" width="28" height="28"> Seven Time: Universal API

Manage projects, work orders, time logs, and customers

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sevenTime/latest
- **Category:** Support / Field Service
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://seventime.se
- **Vendor API docs:** https://docs.seventime.se

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Customer

| Action | Method | Description |
| --- | --- | --- |
| [List Customers](actions/list-customers.md) | GET | Retrieves customers from a Seven Time workspace. |

### Department

| Action | Method | Description |
| --- | --- | --- |
| [List Departments](actions/list-departments.md) | GET | Retrieves departments from a Seven Time workspace. |

### Invoice Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Invoice Tags](actions/list-invoice-tags.md) | GET | Retrieves invoice tags from Seven Time. |

### Machine Type

| Action | Method | Description |
| --- | --- | --- |
| [List Machine Types](actions/list-machine-types.md) | GET | Retrieves machine types from Seven Time. |

### Price List

| Action | Method | Description |
| --- | --- | --- |
| [List Price Lists](actions/list-price-lists.md) | GET | Retrieves price lists from Seven Time. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from a Seven Time workspace. |

### Project Status

| Action | Method | Description |
| --- | --- | --- |
| [List Project Statuses](actions/list-project-statuses.md) | GET | Retrieves project statuses from Seven Time. |

### Project Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Project Tags](actions/list-project-tags.md) | GET | Retrieves project tags from Seven Time. |

### Project Type

| Action | Method | Description |
| --- | --- | --- |
| [List Project Types](actions/list-project-types.md) | GET | Retrieves project types from Seven Time. |

### Quote Category

| Action | Method | Description |
| --- | --- | --- |
| [List Quote Categories](actions/list-quote-categories.md) | GET | Retrieves quote categories from Seven Time. |

### Quote Template

| Action | Method | Description |
| --- | --- | --- |
| [List Quote Templates](actions/list-quote-templates.md) | GET | Retrieves quote templates from Seven Time. |

### Result Unit

| Action | Method | Description |
| --- | --- | --- |
| [List Result Units](actions/list-result-units.md) | GET | Retrieves result units from Seven Time. |

### Time Category

| Action | Method | Description |
| --- | --- | --- |
| [List Time Categories](actions/list-time-categories.md) | GET | Retrieves time categories from Seven Time. |

### Time Log

| Action | Method | Description |
| --- | --- | --- |
| [List Time Logs](actions/list-time-logs.md) | GET | Retrieves time logs from a Seven Time workspace. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user from a Seven Time workspace. |
| [List Users](actions/list-users.md) | GET | Retrieves users from a Seven Time workspace. |

### User Role

| Action | Method | Description |
| --- | --- | --- |
| [List User Roles](actions/list-user-roles.md) | GET | Retrieves user roles from Seven Time. |

### User Salary Type

| Action | Method | Description |
| --- | --- | --- |
| [List User Salary Types](actions/list-user-salary-types.md) | GET | Retrieves user salary types from Seven Time. |

### User Skill

| Action | Method | Description |
| --- | --- | --- |
| [List User Skills](actions/list-user-skills.md) | GET | Retrieves user skills from Seven Time. |

### User Work Type

| Action | Method | Description |
| --- | --- | --- |
| [List User Work Types](actions/list-user-work-types.md) | GET | Retrieves user work types from Seven Time. |

### Work Order Status

| Action | Method | Description |
| --- | --- | --- |
| [List Work Order Statuses](actions/list-work-order-statuses.md) | GET | Retrieves work order statuses from Seven Time. |

### Work Order Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Work Order Tags](actions/list-work-order-tags.md) | GET | Retrieves work order tags from Seven Time. |

### Work Order Type

| Action | Method | Description |
| --- | --- | --- |
| [List Work Order Types](actions/list-work-order-types.md) | GET | Retrieves work order types from Seven Time. |

### Work Schedule

| Action | Method | Description |
| --- | --- | --- |
| [List Work Schedules](actions/list-work-schedules.md) | GET | Retrieves work schedules from Seven Time. |

