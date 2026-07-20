# <img src="https://images.mindcloud.co/apps/icons/screenshot-2026-03-24-at-14_1774373326970.png" alt="Mural logo" width="28" height="28"> Mural: Universal API

Create murals, manage rooms, and use collaboration templates

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mural/latest
- **Category:** Productivity / Project Management
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mural.co
- **Vendor API docs:** https://developers.mural.co/public/reference/intro

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mural/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder in Room](actions/create-folder-in-room.md) | POST | Creates a new folder in a Mural room. |
| [List Folders for Room](actions/list-folders-for-room.md) | GET | Finds folders in Mural for a room. |

### Mural

| Action | Method | Description |
| --- | --- | --- |
| [Create Mural](actions/create-mural.md) | POST | Creates a new mural in Mural. |
| [Create Mural from Template](actions/create-mural-from-template.md) | POST | Creates a new mural in Mural from a template. |
| [Duplicate Mural](actions/duplicate-mural.md) | POST | Creates a new mural in Mural by duplicating another mural. |
| [Export Mural to File](actions/export-mural-to-file.md) | POST | Creates a new mural export in Mural. |
| [Get Mural](actions/get-mural.md) | GET | Retrieves a mural from Mural by ID. |
| [List Murals for Room](actions/list-murals-for-room.md) | GET | Finds murals in Mural for a room. |
| [List Murals for Workspace](actions/list-murals-for-workspace.md) | GET | Finds murals in Mural for a workspace. |
| [List Recently Opened Murals for Workspace](actions/list-recently-opened-murals-for-workspace.md) | GET | Finds recently opened murals in Mural for a workspace. |
| [Search Murals](actions/search-murals.md) | GET | Finds murals in Mural by search query. |
| [Update Mural](actions/update-mural.md) | PUT | Updates an existing mural in Mural. |

### Room

| Action | Method | Description |
| --- | --- | --- |
| [Create Room](actions/create-room.md) | POST | Creates a new room in Mural. |
| [Get Room](actions/get-room.md) | GET | Retrieves a room from Mural by ID. |
| [List Open Rooms for Workspace](actions/list-open-rooms-for-workspace.md) | GET | Finds open rooms in Mural for a workspace. |
| [List Rooms for Workspace](actions/list-rooms-for-workspace.md) | GET | Finds rooms in Mural for a workspace. |
| [Search Rooms](actions/search-rooms.md) | GET | Finds rooms in Mural by search query. |
| [Update Room](actions/update-room.md) | PUT | Updates an existing room in Mural. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Default and Custom Templates for Workspace](actions/list-default-and-custom-templates-for-workspace.md) | GET | Finds default and custom templates in Mural for a workspace. |
| [List Recent Templates for Workspace](actions/list-recent-templates-for-workspace.md) | GET | Finds recent templates in Mural for a workspace. |

### Url

| Action | Method | Description |
| --- | --- | --- |
| [Get Export URL](actions/get-export-url.md) | GET | Retrieves a mural export URL from Mural. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Mural. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Mural by ID. |
| [List Workspaces](actions/list-workspaces.md) | GET | Finds workspaces in Mural for the current user. |

