# <img src="https://images.mindcloud.co/apps/icons/lark-drive_1776267152822.png" alt="Lark Drive logo" width="28" height="28"> Lark Drive: Universal API

Browse Lark Drive files and folders

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/larkDrive/latest
- **Category:** Content & Files / Storage
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.larksuite.com
- **Vendor API docs:** https://open.larksuite.com/document

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check File Task](actions/check-file-task.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/larkDrive/latest/actions/check-file-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Tenant Access Token](actions/get-tenant-access-token.md) | POST |  |
| [Refresh User Token](actions/refresh-user-token.md) | PUT |  |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Copy File](actions/copy-file.md) | POST |  |
| [Delete File or Folder](actions/delete-file-or-folder.md) | DELETE |  |
| [Download File](actions/download-file.md) | GET |  |
| [Get File Statistics](actions/get-file-statistics.md) | GET |  |
| [List Files](actions/list-files.md) | GET |  |
| [Move File or Folder](actions/move-file-or-folder.md) | PUT |  |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST |  |
| [Get Root Folder Meta](actions/get-root-folder-meta.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Check File Task](actions/check-file-task.md) | GET |  |

