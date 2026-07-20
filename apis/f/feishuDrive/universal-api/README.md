# <img src="https://images.mindcloud.co/apps/icons/feishu-document-1776187446252_1776193511239.png" alt="Feishu Drive logo" width="28" height="28"> Feishu Drive: Universal API

Access Feishu Drive files and metadata in MindCloud, including uploads, downloads, copy, move, import, export, and related Drive file operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/feishuDrive/latest
- **Category:** Content & Files / Storage
- **Actions:** 12
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.feishu.cn
- **Vendor API docs:** https://open.feishu.cn/document/uAjLw4CM/ukTMukTMukTM/reference/drive-v1/file/file-overview

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check File Task](actions/check-file-task.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/feishuDrive/latest/actions/check-file-task?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (12)

### Access Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Get Tenant Access Token](actions/get-tenant-access-token.md) | POST | Retrieves a tenant access token for Feishu. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Copy File](actions/copy-file.md) | POST | Creates a file copy in Feishu Drive. |
| [Create File Shortcut](actions/create-file-shortcut.md) | POST | Creates a file shortcut in Feishu Drive. |
| [Delete File or Folder](actions/delete-file-or-folder.md) | DELETE | Deletes a file or folder from Feishu Drive. |
| [Download File](actions/download-file.md) | GET | Retrieves a file download from Feishu Drive. |
| [Get File Metadata](actions/get-file-metadata.md) | GET | Retrieves file metadata from Feishu Drive. |
| [Get File Statistics](actions/get-file-statistics.md) | GET | Retrieves file statistics from Feishu Drive. |
| [List Files](actions/list-files.md) | GET | Retrieves files from Feishu Drive. |
| [Move File or Folder](actions/move-file-or-folder.md) | PUT | Moves a file or folder in Feishu Drive. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Feishu Drive. |
| [Get Root Folder Meta](actions/get-root-folder-meta.md) | GET | Retrieves root folder metadata from Feishu Drive. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Check File Task](actions/check-file-task.md) | GET | Retrieves a file task status from Feishu Drive. |

