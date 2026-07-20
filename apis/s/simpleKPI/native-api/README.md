# SimpleKPI: Native API Reference

A consolidated summary of SimpleKPI's API configuration and 42 documented operations, with links to official documentation.

- **Official docs:** https://support.simplekpi.com/Developers
- **API base URL:** `https://{subdomain}.simplekpi.com/api/`

## Authentication

### Basic

Authenticate to the SimpleKPI API with your SimpleKPI login email as the Basic auth username, your API token as the Basic auth password, and your tenant subdomain.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Subdomain:** `subdomain` · required · Your SimpleKPI tenant subdomain (for https://<subdomain>.simplekpi.com).

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://support.simplekpi.com/Developers)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (42 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Group](actions/create-group.md) | `POST groups` | [docs](https://support.simplekpi.com/Developers/Groups) |
| [Create Group Item](actions/create-group-item.md) | `POST groups/:groupId/items` | [docs](https://support.simplekpi.com/Developers/GroupsGroupItems) |
| [Create KPI](actions/create-kpi.md) | `POST kpis` | [docs](https://support.simplekpi.com/Developers/KPIs) |
| [Create KPI Entry](actions/create-kpi-entry.md) | `POST kpientries` | [docs](https://support.simplekpi.com/Developers/KPIEntries) |
| [Create User Group Item](actions/create-user-group-item.md) | `POST users/:userId/groupitems` | [docs](https://support.simplekpi.com/Developers/UsersGroupItems) |
| [Create User KPI](actions/create-user-kpi.md) | `POST users/:userId/kpis` | [docs](https://support.simplekpi.com/Developers/UsersKPIs) |
| [Delete Group](actions/delete-group.md) | `DELETE groups/:id` | [docs](https://support.simplekpi.com/Developers/Groups) |
| [Delete Group Item](actions/delete-group-item.md) | `DELETE groups/:groupId/items/:id` | [docs](https://support.simplekpi.com/Developers/GroupsGroupItems) |
| [Delete KPI](actions/delete-kpi.md) | `DELETE kpis/:id` | [docs](https://support.simplekpi.com/Developers/KPIs) |
| [Delete KPI Entry](actions/delete-kpi-entry.md) | `DELETE kpientries/:id` | [docs](https://support.simplekpi.com/Developers/KPIEntries) |
| [Delete User Group Item](actions/delete-user-group-item.md) | `DELETE users/:userId/groupitems/:id` | [docs](https://support.simplekpi.com/Developers/UsersGroupItems) |
| [Delete User KPI](actions/delete-user-kpi.md) | `DELETE users/:userId/kpis/:id` | [docs](https://support.simplekpi.com/Developers/UsersKPIs) |
| [Get Group](actions/get-group.md) | `GET groups/:id` | [docs](https://support.simplekpi.com/Developers/Groups) |
| [Get Group Item](actions/get-group-item.md) | `GET groups/:groupId/items/:id` | [docs](https://support.simplekpi.com/Developers/GroupsGroupItems) |
| [Get KPI](actions/get-kpi.md) | `GET kpis/:id` | [docs](https://support.simplekpi.com/Developers/KPIs) |
| [Get KPI Category](actions/get-kpi-category.md) | `GET kpicategories/:id` | [docs](https://support.simplekpi.com/Developers/KPICategories) |
| [Get KPI Entry](actions/get-kpi-entry.md) | `GET kpientries/:id` | [docs](https://support.simplekpi.com/Developers/KPIEntries) |
| [Get KPI Frequency](actions/get-kpi-frequency.md) | `GET kpifrequencies/:id` | [docs](https://support.simplekpi.com/Developers/KPIFrequencies) |
| [Get KPI Icon](actions/get-kpi-icon.md) | `GET kpiicons/:id` | [docs](https://support.simplekpi.com/Developers/KPIIcons) |
| [Get KPI Unit](actions/get-kpi-unit.md) | `GET kpiunits/:id` | [docs](https://support.simplekpi.com/Developers/KPIUnits) |
| [Get User](actions/get-user.md) | `GET users/:id` | [docs](https://support.simplekpi.com/Developers/Users) |
| [Get User Group Item](actions/get-user-group-item.md) | `GET users/:userId/groupitems/:id` | [docs](https://support.simplekpi.com/Developers/UsersGroupItems) |
| [Get User KPI](actions/get-user-kpi.md) | `GET users/:userId/kpis/:id` | [docs](https://support.simplekpi.com/Developers/UsersKPIs) |
| [List Group Items](actions/list-group-items.md) | `GET groups/:groupId/items` | [docs](https://support.simplekpi.com/Developers/GroupsGroupItems) |
| [List Groups](actions/list-groups.md) | `GET groups` | [docs](https://support.simplekpi.com/Developers/Groups) |
| [List KPI Categories](actions/list-kpi-categories.md) | `GET kpicategories` | [docs](https://support.simplekpi.com/Developers/KPICategories) |
| [List KPI Category KPIs](actions/list-kpi-category-kpis.md) | `GET kpicategories/:categoryId/kpis` | [docs](https://support.simplekpi.com/Developers/KPICategoriesKPIs) |
| [List KPI Entries](actions/list-kpi-entries.md) | `GET kpientries` | [docs](https://support.simplekpi.com/Developers/KPIEntries) |
| [List KPI Frequencies](actions/list-kpi-frequencies.md) | `GET kpifrequencies` | [docs](https://support.simplekpi.com/Developers/KPIFrequencies) |
| [List KPI Icons](actions/list-kpi-icons.md) | `GET kpiicons` | [docs](https://support.simplekpi.com/Developers/KPIIcons) |
| [List KPI Units](actions/list-kpi-units.md) | `GET kpiunits` | [docs](https://support.simplekpi.com/Developers/KPIUnits) |
| [List KPIs](actions/list-kpis.md) | `GET kpis` | [docs](https://support.simplekpi.com/Developers/KPIs) |
| [List Report Data Entries](actions/list-report-data-entries.md) | `GET reports/AllDataEntries` | [docs](https://support.simplekpi.com/Developers/Reports) |
| [List Reports](actions/list-reports.md) | `GET reports` | [docs](https://support.simplekpi.com/Developers/Reports) |
| [List User Group Items](actions/list-user-group-items.md) | `GET users/:userId/groupitems` | [docs](https://support.simplekpi.com/Developers/UsersGroupItems) |
| [List User KPIs](actions/list-user-kpis.md) | `GET users/:userId/kpis` | [docs](https://support.simplekpi.com/Developers/UsersKPIs) |
| [List Users](actions/list-users.md) | `GET users` | [docs](https://support.simplekpi.com/Developers/Users) |
| [Update Group](actions/update-group.md) | `PUT groups/:id` | [docs](https://support.simplekpi.com/Developers/Groups) |
| [Update Group Item](actions/update-group-item.md) | `PUT groups/:groupId/items/:id` | [docs](https://support.simplekpi.com/Developers/GroupsGroupItems) |
| [Update KPI](actions/update-kpi.md) | `PUT kpis/:id` | [docs](https://support.simplekpi.com/Developers/KPIs) |
| [Update KPI Entry](actions/update-kpi-entry.md) | `PUT kpientries/:id` | [docs](https://support.simplekpi.com/Developers/KPIEntries) |
| [Update User KPI](actions/update-user-kpi.md) | `PUT users/:userId/kpis/:id` | [docs](https://support.simplekpi.com/Developers/UsersKPIs) |
