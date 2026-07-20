# ApptiveGrid: Native API Reference

A consolidated summary of ApptiveGrid's API configuration and 22 documented operations, with links to official documentation.

- **Official docs:** https://pub.dev/documentation/apptive_grid_core/latest/
- **API base URL:** `https://app.apptivegrid.de`

## Authentication

### Basic Authentication

MindCloud Username maps to the ApptiveGrid authorization key, and MindCloud Password maps to the ApptiveGrid API password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://github.com/ApptiveGrid/ApptiveGrid-flutter/blob/main/packages/apptive_grid_core/lib/src/network/authentication/apptive_grid_authentication_options.dart)

## Endpoints (22 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Grid](actions/create-grid.md) | `POST /api/users/:user_id/spaces/:space_id/grids` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#addGrid) |
| [Create Space](actions/create-space.md) | `POST /api/users/:user_id/spaces` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#addSpace) |
| [Delete Grid](actions/delete-grid.md) | `DELETE /api/users/:user_id/spaces/:space_id/grids/:grid_id` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#remove) |
| [Delete Space](actions/delete-space.md) | `DELETE /api/users/:user_id/spaces/:space_id` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#remove) |
| [Get Current User](actions/get-current-user.md) | `GET /api/users/me` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveGridClient/getMe.html) |
| [Get Grid Details](actions/get-grid-details.md) | `GET /api/users/:user_id/spaces/:space_id/grids/:grid_id` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/Grid-class.html) |
| [Get Grid Schema](actions/get-grid-schema.md) | `GET /api/users/:user_id/spaces/:space_id/grids/:grid_id/schema` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#schema) |
| [Get Space Details](actions/get-space-details.md) | `GET /api/users/:user_id/spaces/:space_id` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/Space-class.html) |
| [Get User Details](actions/get-user-details.md) | `GET /api/users/:user_id` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/User-class.html) |
| [List Access Credentials](actions/list-access-credentials.md) | `GET /api/users/:user_id/accessKeys` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#accessCredentials) |
| [List Flows](actions/list-flows.md) | `GET /api/users/:user_id/flows` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#flows) |
| [List Grid Forms](actions/list-grid-forms.md) | `GET /api/users/:user_id/spaces/:space_id/grids/:grid_id/forms` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#forms) |
| [List Grid Rows](actions/list-grid-rows.md) | `GET /api/users/:user_id/spaces/:space_id/grids/:grid_id/entities` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#entities) |
| [List Grid Stateful Views](actions/list-grid-stateful-views.md) | `GET /api/users/:user_id/spaces/:space_id/grids/:grid_id/sviews` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#sviews) |
| [List Grid Views](actions/list-grid-views.md) | `GET /api/users/:user_id/spaces/:space_id/grids/:grid_id/views` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#views) |
| [List Grid Virtual Grids](actions/list-grid-virtual-grids.md) | `GET /api/users/:user_id/spaces/:space_id/grids/:grid_id/virtualgrids` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#virtualGrids) |
| [List Space Flows](actions/list-space-flows.md) | `GET /api/users/:user_id/spaces/:space_id/flows` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#flows) |
| [List Space Grids](actions/list-space-grids.md) | `GET /api/users/:user_id/spaces/:space_id/grids` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#grids) |
| [List Space Hooks](actions/list-space-hooks.md) | `GET /api/users/:user_id/spaces/:space_id/hooks` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#hooks) |
| [List Space Invitations](actions/list-space-invitations.md) | `GET /api/users/:user_id/spaces/:space_id/invitations` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#invitations) |
| [List Space Shares](actions/list-space-shares.md) | `GET /api/users/:user_id/spaces/:space_id/shares` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#shares) |
| [List Spaces](actions/list-spaces.md) | `GET /api/users/:user_id/spaces` | [docs](https://pub.dev/documentation/apptive_grid_core/latest/apptive_grid_core/ApptiveLinkType.html#spaces) |
