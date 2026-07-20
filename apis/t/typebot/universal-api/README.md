# <img src="https://images.mindcloud.co/apps/icons/images-2_1773785339681.png" alt="Typebot logo" width="28" height="28"> Typebot: Universal API

Manage workspaces, folders, typebots, and team members

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/typebot/latest
- **Category:** Communication / Team Messaging
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://typebot.io
- **Vendor API docs:** https://docs.typebot.io/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/typebot/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST |  |
| [Get Folder](actions/get-folder.md) | GET |  |
| [List Folders](actions/list-folders.md) | GET |  |
| [Update Folder](actions/update-folder.md) | PUT |  |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Typebot](actions/create-typebot.md) | POST |  |
| [Delete Typebot](actions/delete-typebot.md) | DELETE |  |
| [Get Published Typebot](actions/get-published-typebot.md) | GET |  |
| [Get Result](actions/get-result.md) | GET |  |
| [Get Result Transcript](actions/get-result-transcript.md) | GET |  |
| [Get Results Stats](actions/get-results-stats.md) | GET |  |
| [Get Typebot](actions/get-typebot.md) | GET |  |
| [Import Typebot](actions/import-typebot.md) | POST |  |
| [List Result Logs](actions/list-result-logs.md) | GET |  |
| [List Results](actions/list-results.md) | GET |  |
| [List Typebots](actions/list-typebots.md) | GET |  |
| [Publish Typebot](actions/publish-typebot.md) | PUT |  |
| [Unpublish Typebot](actions/unpublish-typebot.md) | PUT |  |
| [Update Typebot](actions/update-typebot.md) | PUT |  |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Workspace Members](actions/list-workspace-members.md) | GET |  |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST |  |
| [Get Workspace](actions/get-workspace.md) | GET |  |
| [List Workspaces](actions/list-workspaces.md) | GET |  |
| [Update Workspace](actions/update-workspace.md) | PUT |  |

