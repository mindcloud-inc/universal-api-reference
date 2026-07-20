# <img src="https://images.mindcloud.co/apps/icons/9086360_1774549403719.png" alt="SimpleKPI logo" width="28" height="28"> SimpleKPI: Universal API

SimpleKPI is a KPI tracking and reporting platform for managing users, groups, KPIs, reports, and KPI entry data through the SimpleKPI REST API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/simpleKPI/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 42
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.simplekpi.com
- **Vendor API docs:** https://support.simplekpi.com/Developers

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Users](actions/list-users.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleKPI/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (42)

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | POST | Creates a new group in SimpleKPI. |
| [Delete Group](actions/delete-group.md) | DELETE | Deletes an existing group from SimpleKPI. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group record from SimpleKPI. |
| [List Groups](actions/list-groups.md) | GET | Retrieves group records from a SimpleKPI account. |
| [Update Group](actions/update-group.md) | PUT | Updates an existing group in SimpleKPI. |

### Group Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Group Item](actions/create-group-item.md) | POST | Creates a new group item in SimpleKPI. |
| [Delete Group Item](actions/delete-group-item.md) | DELETE | Deletes an existing group item from SimpleKPI. |
| [Get Group Item](actions/get-group-item.md) | GET | Retrieves a group item from SimpleKPI. |
| [List Group Items](actions/list-group-items.md) | GET | Retrieves group items from a SimpleKPI group. |
| [Update Group Item](actions/update-group-item.md) | PUT | Updates an existing group item in SimpleKPI. |

### Kpi

| Action | Method | Description |
| --- | --- | --- |
| [Create KPI](actions/create-kpi.md) | POST | Creates a new KPI in SimpleKPI. |
| [Delete KPI](actions/delete-kpi.md) | DELETE | Deletes an existing KPI from SimpleKPI. |
| [Get KPI](actions/get-kpi.md) | GET | Retrieves a KPI record from SimpleKPI. |
| [List KPI Category KPIs](actions/list-kpi-category-kpis.md) | GET | Retrieves KPIs from a SimpleKPI KPI category. |
| [List KPIs](actions/list-kpis.md) | GET | Retrieves KPI records from a SimpleKPI account. |
| [Update KPI](actions/update-kpi.md) | PUT | Updates an existing KPI in SimpleKPI. |

### Kpi Category

| Action | Method | Description |
| --- | --- | --- |
| [Get KPI Category](actions/get-kpi-category.md) | GET | Retrieves a KPI category from SimpleKPI. |
| [List KPI Categories](actions/list-kpi-categories.md) | GET | Retrieves KPI category records from SimpleKPI. |

### Kpi Entry

| Action | Method | Description |
| --- | --- | --- |
| [Create KPI Entry](actions/create-kpi-entry.md) | POST | Creates a new KPI entry in SimpleKPI. |
| [Delete KPI Entry](actions/delete-kpi-entry.md) | DELETE | Deletes an existing KPI entry from SimpleKPI. |
| [Get KPI Entry](actions/get-kpi-entry.md) | GET | Retrieves a KPI entry from SimpleKPI. |
| [List KPI Entries](actions/list-kpi-entries.md) | GET | Retrieves KPI entries from a SimpleKPI account. |
| [Update KPI Entry](actions/update-kpi-entry.md) | PUT | Updates an existing KPI entry in SimpleKPI. |

### Kpi Frequency

| Action | Method | Description |
| --- | --- | --- |
| [Get KPI Frequency](actions/get-kpi-frequency.md) | GET | Retrieves a KPI frequency from SimpleKPI. |
| [List KPI Frequencies](actions/list-kpi-frequencies.md) | GET | Retrieves KPI frequency records from SimpleKPI. |

### Kpi Icon

| Action | Method | Description |
| --- | --- | --- |
| [Get KPI Icon](actions/get-kpi-icon.md) | GET | Retrieves a KPI icon from SimpleKPI. |
| [List KPI Icons](actions/list-kpi-icons.md) | GET | Retrieves KPI icon records from SimpleKPI. |

### Kpi Unit

| Action | Method | Description |
| --- | --- | --- |
| [Get KPI Unit](actions/get-kpi-unit.md) | GET | Retrieves a KPI unit from SimpleKPI. |
| [List KPI Units](actions/list-kpi-units.md) | GET | Retrieves KPI unit records from SimpleKPI. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [List Reports](actions/list-reports.md) | GET |  |

### Report Data Entry

| Action | Method | Description |
| --- | --- | --- |
| [List Report Data Entries](actions/list-report-data-entries.md) | GET | Retrieves report data entries from SimpleKPI. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user record from SimpleKPI. |
| [List Users](actions/list-users.md) | GET | Retrieves user records from a SimpleKPI account. |

### User Group Item

| Action | Method | Description |
| --- | --- | --- |
| [Create User Group Item](actions/create-user-group-item.md) | POST | Creates a group item for a SimpleKPI user. |
| [Delete User Group Item](actions/delete-user-group-item.md) | DELETE | Deletes a group item from a SimpleKPI user. |
| [Get User Group Item](actions/get-user-group-item.md) | GET | Retrieves a user's group item from SimpleKPI. |
| [List User Group Items](actions/list-user-group-items.md) | GET | Retrieves group items assigned to a SimpleKPI user. |

### User Kpi

| Action | Method | Description |
| --- | --- | --- |
| [Create User KPI](actions/create-user-kpi.md) | POST | Creates a KPI for a SimpleKPI user. |
| [Delete User KPI](actions/delete-user-kpi.md) | DELETE | Deletes a KPI from a SimpleKPI user. |
| [Get User KPI](actions/get-user-kpi.md) | GET | Retrieves a KPI assigned to a SimpleKPI user. |
| [List User KPIs](actions/list-user-kpis.md) | GET | Retrieves KPIs assigned to a SimpleKPI user. |
| [Update User KPI](actions/update-user-kpi.md) | PUT | Updates a KPI for a SimpleKPI user. |

