# <img src="https://images.mindcloud.co/apps/icons/favicon_1775482764551.png" alt="ApptiveGrid logo" width="28" height="28"> ApptiveGrid: Universal API

Build, manage, and automate structured business data in ApptiveGrid.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/apptiveGrid/latest
- **Category:** IT Operations / Database
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.apptivegrid.de/
- **Vendor API docs:** https://pub.dev/documentation/apptive_grid_core/latest/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/apptiveGrid/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Access Credential

| Action | Method | Description |
| --- | --- | --- |
| [List Access Credentials](actions/list-access-credentials.md) | GET | Retrieves access credentials from ApptiveGrid. |

### Current User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from ApptiveGrid. |

### Flow

| Action | Method | Description |
| --- | --- | --- |
| [List Flows](actions/list-flows.md) | GET | Retrieves flows from ApptiveGrid. |
| [List Space Flows](actions/list-space-flows.md) | GET | Retrieves flows from an ApptiveGrid space. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [List Grid Forms](actions/list-grid-forms.md) | GET | Retrieves forms from an ApptiveGrid grid. |

### Grid

| Action | Method | Description |
| --- | --- | --- |
| [Create Grid](actions/create-grid.md) | POST | Creates a new grid in ApptiveGrid. |
| [Delete Grid](actions/delete-grid.md) | DELETE | Deletes an existing grid from ApptiveGrid. |
| [Get Grid Details](actions/get-grid-details.md) | GET | Retrieves a grid from ApptiveGrid. |
| [List Space Grids](actions/list-space-grids.md) | GET | Retrieves grids from an ApptiveGrid space. |

### Grid Row

| Action | Method | Description |
| --- | --- | --- |
| [List Grid Rows](actions/list-grid-rows.md) | GET | Retrieves grid rows from ApptiveGrid. |

### Grid Schema

| Action | Method | Description |
| --- | --- | --- |
| [Get Grid Schema](actions/get-grid-schema.md) | GET | Retrieves a grid schema from ApptiveGrid. |

### Hook

| Action | Method | Description |
| --- | --- | --- |
| [List Space Hooks](actions/list-space-hooks.md) | GET | Retrieves hooks from an ApptiveGrid space. |

### Invitation

| Action | Method | Description |
| --- | --- | --- |
| [List Space Invitations](actions/list-space-invitations.md) | GET | Retrieves invitations from an ApptiveGrid space. |

### Share

| Action | Method | Description |
| --- | --- | --- |
| [List Space Shares](actions/list-space-shares.md) | GET | Retrieves shares from an ApptiveGrid space. |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [Create Space](actions/create-space.md) | POST | Creates a new space in ApptiveGrid. |
| [Delete Space](actions/delete-space.md) | DELETE | Deletes an existing space from ApptiveGrid. |
| [Get Space Details](actions/get-space-details.md) | GET | Retrieves a space from ApptiveGrid. |
| [List Spaces](actions/list-spaces.md) | GET | Retrieves spaces from ApptiveGrid. |

### Stateful View

| Action | Method | Description |
| --- | --- | --- |
| [List Grid Stateful Views](actions/list-grid-stateful-views.md) | GET | Retrieves stateful views from an ApptiveGrid grid. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Details](actions/get-user-details.md) | GET | Retrieves a user from ApptiveGrid. |

### View

| Action | Method | Description |
| --- | --- | --- |
| [List Grid Views](actions/list-grid-views.md) | GET | Retrieves views from an ApptiveGrid grid. |

### Virtual Grid

| Action | Method | Description |
| --- | --- | --- |
| [List Grid Virtual Grids](actions/list-grid-virtual-grids.md) | GET | Retrieves virtual grids from an ApptiveGrid grid. |

