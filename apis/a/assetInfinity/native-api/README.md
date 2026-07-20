# Asset Infinity: Native API Reference

A consolidated summary of Asset Infinity's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://api.assetinfinity.io/index.html
- **OpenAPI specification:** https://api.assetinfinity.io/swagger/BaseApi/swagger.json
- **API base URL:** `https://api.assetinfinity.io/api/`

## Authentication

### JWT Token

Use an Asset Infinity JWT token obtained from the signin endpoint.

### Credentials

- **JWT Token:** `token` · optional · Paste a valid Asset Infinity JWT token from the signin endpoint.

Send these headers with each API request:

```http
Authorization: Bearer <token>
```

[Official authentication documentation](https://support.assetinfinity.com/portal/en/kb/articles/jwt-token-for-authorization-to-asset-infinity)

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Asset Dropdown](actions/get-asset-dropdown.md) | `POST GetAssetDropdown` | [docs](https://api.assetinfinity.io/index.html) |
| [Get Current Session](actions/get-current-session.md) | `GET auth` | [docs](https://support.assetinfinity.com/portal/en/kb/articles/jwt-token-for-authorization-to-asset-infinity) |
| [Get Departments By User](actions/get-departments-by-user.md) | `POST GetDepartmentbyUser` | [docs](https://api.assetinfinity.io/index.html) |
| [Get Items](actions/get-items.md) | `POST GetItem` | [docs](https://api.assetinfinity.io/index.html) |
| [Get Ticket Details](actions/get-ticket-details.md) | `POST GetTicketDetails` | [docs](https://api.assetinfinity.io/index.html) |
| [Get Ticket Group Assignees](actions/get-ticket-group-assignees.md) | `POST GetTicketGroupAssignee` | [docs](https://api.assetinfinity.io/index.html) |
| [Get Ticket Groups](actions/get-ticket-groups.md) | `POST GetTicketGroupAPI` | [docs](https://api.assetinfinity.io/index.html) |
| [Get Ticket Locations](actions/get-ticket-locations.md) | `POST GetTicketLocationTreeView` | [docs](https://api.assetinfinity.io/index.html) |
| [Get Ticket Priorities](actions/get-ticket-priorities.md) | `POST GetTicketPriority` | [docs](https://api.assetinfinity.io/index.html) |
| [Get Ticket Statuses](actions/get-ticket-statuses.md) | `POST GetTicketStatus` | [docs](https://api.assetinfinity.io/index.html) |
| [Get Ticket Type Dropdown](actions/get-ticket-type-dropdown.md) | `POST GetTicketTypeDropDown` | [docs](https://api.assetinfinity.io/index.html) |
| [Get Unit Master](actions/get-unit-master.md) | `POST GetUnitMaster` | [docs](https://api.assetinfinity.io/index.html) |
| [Get User Groups](actions/get-user-groups.md) | `POST GetUserGroupAPI` | [docs](https://api.assetinfinity.io/index.html) |
| [Get Vendors](actions/get-vendors.md) | `POST GetVendor` | [docs](https://api.assetinfinity.io/index.html) |
| [List App Roles](actions/list-app-roles.md) | `POST prcGetAppRoleList_DDL` | [docs](https://api.assetinfinity.io/index.html) |
| [List Assets](actions/list-assets.md) | `POST asset-list` | [docs](https://api.assetinfinity.io/index.html) |
| [List Brands](actions/list-brands.md) | `GET BrandList` | [docs](https://api.assetinfinity.io/index.html) |
| [List Categories](actions/list-categories.md) | `POST Category_Treeview` | [docs](https://api.assetinfinity.io/index.html) |
| [List Conditions](actions/list-conditions.md) | `POST ConditionList` | [docs](https://api.assetinfinity.io/index.html) |
| [List Departments](actions/list-departments.md) | `POST DepartmentList` | [docs](https://api.assetinfinity.io/index.html) |
| [List Locations](actions/list-locations.md) | `POST LocationList_TreeView` | [docs](https://api.assetinfinity.io/index.html) |
| [List Models](actions/list-models.md) | `GET ModelList` | [docs](https://api.assetinfinity.io/index.html) |
| [List Movement Type Statuses](actions/list-movement-type-statuses.md) | `GET MovementTypeStatusList` | [docs](https://api.assetinfinity.io/index.html) |
| [List Movement Types](actions/list-movement-types.md) | `GET MovementTypeList` | [docs](https://api.assetinfinity.io/index.html) |
| [List Parts](actions/list-parts.md) | `POST PartsList` | [docs](https://api.assetinfinity.io/index.html) |
| [List Reason Dropdown](actions/list-reason-dropdown.md) | `GET ReasonDropDown` | [docs](https://api.assetinfinity.io/index.html) |
| [List Reasons](actions/list-reasons.md) | `GET ReasonList` | [docs](https://api.assetinfinity.io/index.html) |
| [List Request Types](actions/list-request-types.md) | `POST RequestTypeList_DDL` | [docs](https://api.assetinfinity.io/index.html) |
| [List Requests](actions/list-requests.md) | `POST RequestList_DDL` | [docs](https://api.assetinfinity.io/index.html) |
| [List Roles](actions/list-roles.md) | `POST RolesList` | [docs](https://api.assetinfinity.io/index.html) |
| [List Status Types](actions/list-status-types.md) | `POST StatusTypes` | [docs](https://api.assetinfinity.io/index.html) |
| [List Statuses](actions/list-statuses.md) | `POST StatusList` | [docs](https://api.assetinfinity.io/index.html) |
| [List Tax Groups](actions/list-tax-groups.md) | `GET TaxGroupList` | [docs](https://api.assetinfinity.io/index.html) |
| [List Tax Settings](actions/list-tax-settings.md) | `GET TaxSettingList` | [docs](https://api.assetinfinity.io/index.html) |
| [List Ticket Type Grid](actions/list-ticket-type-grid.md) | `GET TicketTypeGrid` | [docs](https://api.assetinfinity.io/index.html) |
| [List Ticket Types](actions/list-ticket-types.md) | `GET TicketTypeList` | [docs](https://api.assetinfinity.io/index.html) |
| [List Units](actions/list-units.md) | `POST UnitList` | [docs](https://api.assetinfinity.io/index.html) |
| [List User Group Grid](actions/list-user-group-grid.md) | `POST UserGroupGridView` | [docs](https://api.assetinfinity.io/index.html) |
| [List User Group Types](actions/list-user-group-types.md) | `GET UserGroupType_DDL` | [docs](https://api.assetinfinity.io/index.html) |
| [List Users](actions/list-users.md) | `POST UserList_DDL` | [docs](https://api.assetinfinity.io/index.html) |
| [List Vendors and Customers](actions/list-vendors-and-customers.md) | `POST VendorCustomerList` | [docs](https://api.assetinfinity.io/index.html) |
