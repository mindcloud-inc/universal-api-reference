# <img src="https://images.mindcloud.co/apps/icons/pabbly-hook_1776706885621.png" alt="Pabbly Hook logo" width="28" height="28"> Pabbly Hook: Universal API

Manage, transform, and monitor webhook delivery

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pabblyHook/latest
- **Category:** IT Operations / Integration & Automation
- **Actions:** 18
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.pabbly.com/hook/
- **Vendor API docs:** https://apidocs.pabbly.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get All Folders](actions/get-all-folders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pabblyHook/latest/actions/get-all-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (18)

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Create Connection](actions/create-connection.md) | POST |  |
| [Delete Connections](actions/delete-connections.md) | DELETE |  |
| [Filter Connections](actions/filter-connections.md) | GET |  |
| [Get Connection](actions/get-connection.md) | GET |  |
| [Move Connection To Folder](actions/move-connection-to-folder.md) | PUT |  |
| [Update Connection](actions/update-connection.md) | PUT |  |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [Filter Events](actions/filter-events.md) | GET |  |
| [Retrieve All Events](actions/retrieve-all-events.md) | GET |  |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST |  |
| [Delete Folder](actions/delete-folder.md) | DELETE |  |
| [Get All Folders](actions/get-all-folders.md) | GET |  |
| [Rename Folder](actions/rename-folder.md) | PUT |  |

### Request

| Action | Method | Description |
| --- | --- | --- |
| [Filter Requests](actions/filter-requests.md) | GET |  |
| [Retrieve All Requests](actions/retrieve-all-requests.md) | GET |  |

### Transformation

| Action | Method | Description |
| --- | --- | --- |
| [Create Transformation](actions/create-transformation.md) | POST |  |
| [Get All Transformations](actions/get-all-transformations.md) | GET |  |
| [Get Transformation](actions/get-transformation.md) | GET |  |
| [Update Transformation](actions/update-transformation.md) | PUT |  |

