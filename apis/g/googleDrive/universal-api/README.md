# <img src="https://images.mindcloud.co/apps/icons/google-drive-default_1779719589107.png" alt="Google Drive logo" width="28" height="28"> Google Drive: Universal API

Store files, share folders, collaborate on content, and manage access.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/googleDrive/latest
- **Category:** Content & Files / Storage
- **Actions:** 13
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://drive.google.com/
- **Vendor API docs:** https://developers.google.com/workspace/drive/api/reference/rest/v3

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Folders](actions/list-folders.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/list-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (13)

### Document

| Action | Method | Description |
| --- | --- | --- |
| [List Documents](actions/list-documents.md) | GET | Finds documents in Google Drive by query. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Copy File](actions/copy-file.md) | POST | Creates a copy of a file in Google Drive. |
| [Create File](actions/create-file.md) | POST | Creates a new file in Google Drive. |
| [Export File](actions/export-file.md) | GET | Exports a Google Workspace document from Google Drive. |
| [List Files](actions/list-files.md) | GET | List all Files in your Google Drive. Does not return Folders. Optionally filter for a specific file. |
| [Move File](actions/move-file.md) | PUT | Move a File to a Folder. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new Folder in Google Drive. |
| [Get Parent Folder](actions/get-parent-folder.md) | GET | Returns a Parent Folder for a File or Folder in Google Drive. |
| [List Folders](actions/list-folders.md) | GET | Lists all Google Drive Folders. Optionally search folders you have access to in a Team Drive. |
| [List Shared Drives](actions/list-shared-drives.md) | GET | Retrieves shared drives from Google Drive. |
| [Search Files and Folders](actions/search-files-and-folders.md) | GET | Search Files & Folders in Google Drive. |

### Spreadsheet

| Action | Method | Description |
| --- | --- | --- |
| [List Spreadsheets](actions/list-spreadsheets.md) | GET | Finds spreadsheets in Google Drive by query. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Drive User (Auth)](actions/get-drive-user-auth.md) | GET | Gets information about the authenticated user, the user's Drive, and system capabilities. |

