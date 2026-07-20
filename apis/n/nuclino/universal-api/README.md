# <img src="https://mindcloud.imgix.net/apps/icons/nuclino_1776198680763.png" alt="Nuclino logo" width="28" height="28"> Nuclino: Universal API

A collaborative knowledge management app for teams.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nuclino/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nuclino.com/
- **Vendor API docs:** https://help.nuclino.com/d3a29686-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List teams](actions/list-teams.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/list-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Get file](actions/get-file.md) | GET | Retrieves a file's details from Nuclino. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Create item or collection](actions/create-item-or-collection.md) | POST | Creates a new item or collection in Nuclino. |
| [Delete item or collection](actions/delete-item-or-collection.md) | DELETE | Deletes an existing item or collection from Nuclino. |
| [Get item or collection](actions/get-item-or-collection.md) | GET | Retrieves item or collection details from Nuclino. |
| [List items and collections](actions/list-items-and-collections.md) | GET | Retrieves items and collections from Nuclino. |
| [Search items and collections](actions/search-items-and-collections.md) | GET | Finds items and collections in Nuclino by search query. |
| [Update item or collection](actions/update-item-or-collection.md) | PUT | Updates an existing item or collection in Nuclino. |

### Teams

| Action | Method | Description |
| --- | --- | --- |
| [Get team](actions/get-team.md) | GET | Retrieves a team's details from Nuclino. |
| [List teams](actions/list-teams.md) | GET | Retrieves a list of teams from Nuclino. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get user](actions/get-user.md) | GET | Retrieves a user's details from Nuclino. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get workspace](actions/get-workspace.md) | GET | Retrieves a workspace's details from Nuclino. |
| [List workspaces](actions/list-workspaces.md) | GET | Retrieves a list of workspaces from Nuclino. |

