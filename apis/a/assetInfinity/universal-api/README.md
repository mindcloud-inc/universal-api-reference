# <img src="https://images.mindcloud.co/apps/icons/asset-infinity_1775493253588.png" alt="Asset Infinity logo" width="28" height="28"> Asset Infinity: Universal API

Asset Infinity is an asset management platform for tracking assets, inventory, locations, departments, vendors, tickets, and related operational metadata.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/assetInfinity/latest
- **Category:** IT Operations / IT Service Management
- **Actions:** 41
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.assetinfinity.com
- **Vendor API docs:** https://api.assetinfinity.io/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current Session](actions/get-current-session.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/get-current-session?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (41)

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Get Asset Dropdown](actions/get-asset-dropdown.md) | GET | Retrieves asset dropdown options from Asset Infinity. |
| [List Assets](actions/list-assets.md) | GET | Retrieves assets from Asset Infinity. |

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [List Categories](actions/list-categories.md) | GET | Retrieves categories from Asset Infinity. |

### Departments

| Action | Method | Description |
| --- | --- | --- |
| [Get Departments By User](actions/get-departments-by-user.md) | GET | Retrieves departments for a user in Asset Infinity. |
| [List Departments](actions/list-departments.md) | GET | Retrieves departments from Asset Infinity. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Items](actions/get-items.md) | GET | Retrieves items from Asset Infinity. |
| [List Brands](actions/list-brands.md) | GET | Retrieves brands from Asset Infinity. |
| [List Models](actions/list-models.md) | GET | Retrieves models from Asset Infinity. |
| [List Parts](actions/list-parts.md) | GET | Retrieves parts from Asset Infinity. |

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket Locations](actions/get-ticket-locations.md) | GET | Retrieves ticket locations from Asset Infinity. |
| [List Locations](actions/list-locations.md) | GET | Retrieves locations from Asset Infinity. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List App Roles](actions/list-app-roles.md) | GET | Retrieves app roles from Asset Infinity. |
| [List Roles](actions/list-roles.md) | GET | Retrieves roles from Asset Infinity. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [List Status Types](actions/list-status-types.md) | GET | Retrieves status types from Asset Infinity. |
| [List Statuses](actions/list-statuses.md) | GET | Retrieves statuses from Asset Infinity. |

### Stock Movements

| Action | Method | Description |
| --- | --- | --- |
| [List Movement Type Statuses](actions/list-movement-type-statuses.md) | GET | Retrieves movement type statuses from Asset Infinity. |
| [List Movement Types](actions/list-movement-types.md) | GET | Retrieves movement types from Asset Infinity. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Get User Groups](actions/get-user-groups.md) | GET | Retrieves user groups from Asset Infinity. |
| [List User Group Grid](actions/list-user-group-grid.md) | GET | Retrieves user groups for the Asset Infinity grid. |
| [List User Group Types](actions/list-user-group-types.md) | GET | Retrieves user group types from Asset Infinity. |

### Tickets

| Action | Method | Description |
| --- | --- | --- |
| [Get Ticket Details](actions/get-ticket-details.md) | GET | Retrieves ticket details from Asset Infinity. |
| [Get Ticket Groups](actions/get-ticket-groups.md) | GET | Retrieves ticket groups from Asset Infinity. |
| [Get Ticket Priorities](actions/get-ticket-priorities.md) | GET | Retrieves ticket priorities from Asset Infinity. |
| [Get Ticket Statuses](actions/get-ticket-statuses.md) | GET | Retrieves ticket statuses from Asset Infinity. |
| [Get Ticket Type Dropdown](actions/get-ticket-type-dropdown.md) | GET | Retrieves ticket type dropdown options from Asset Infinity. |
| [List Request Types](actions/list-request-types.md) | GET | Retrieves request types from Asset Infinity. |
| [List Requests](actions/list-requests.md) | GET | Retrieves requests from Asset Infinity. |
| [List Ticket Type Grid](actions/list-ticket-type-grid.md) | GET | Retrieves ticket types for the Asset Infinity grid. |
| [List Ticket Types](actions/list-ticket-types.md) | GET | Retrieves ticket types from Asset Infinity. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Unit Master](actions/get-unit-master.md) | GET | Retrieves unit master records from Asset Infinity. |
| [List Conditions](actions/list-conditions.md) | GET | Retrieves conditions from Asset Infinity. |
| [List Reason Dropdown](actions/list-reason-dropdown.md) | GET | Retrieves reason dropdown options from Asset Infinity. |
| [List Reasons](actions/list-reasons.md) | GET | Retrieves reasons from Asset Infinity. |
| [List Tax Groups](actions/list-tax-groups.md) | GET | Retrieves tax groups from Asset Infinity. |
| [List Tax Settings](actions/list-tax-settings.md) | GET | Retrieves tax settings from Asset Infinity. |
| [List Units](actions/list-units.md) | GET | Retrieves units from Asset Infinity. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current Session](actions/get-current-session.md) | GET | Retrieves current session details from Asset Infinity. |
| [Get Ticket Group Assignees](actions/get-ticket-group-assignees.md) | GET | Retrieves ticket group assignees from Asset Infinity. |
| [List Users](actions/list-users.md) | GET | Retrieves users from Asset Infinity. |

### Vendors

| Action | Method | Description |
| --- | --- | --- |
| [Get Vendors](actions/get-vendors.md) | GET | Retrieves vendors from Asset Infinity. |
| [List Vendors and Customers](actions/list-vendors-and-customers.md) | GET | Retrieves vendors and customers from Asset Infinity. |

