# <img src="https://images.mindcloud.co/apps/icons/dropbox_1772821255542.png" alt="Dropbox logo" width="28" height="28"> Dropbox: Universal API

Store files, sync folders, share content, and manage links

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dropbox/latest
- **Category:** Content & Files / Storage
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dropbox.com
- **Vendor API docs:** https://www.dropbox.com/developers/documentation/http/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Continue Folder Listing](actions/continue-folder-listing.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/continue-folder-listing?connectionId=$CONNECTION_ID&cursor=ZtkX9_EHj3x7PMkVuFIhwKYXEpwpLwyxp9vMKomUhllil9q7eWiAu" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves an account's details from Dropbox. |
| [Get Current Account](actions/get-current-account.md) | GET | Retrieves the current account details from Dropbox. |

### Downloaded File

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Retrieves a file's contents from Dropbox. |

### File Member

| Action | Method | Description |
| --- | --- | --- |
| [Add File Members](actions/add-file-members.md) | POST | Adds members to a shared file in Dropbox. |

### File Request

| Action | Method | Description |
| --- | --- | --- |
| [Create File Request](actions/create-file-request.md) | POST | Creates a file request in Dropbox. |
| [Get File Request](actions/get-file-request.md) | GET | Retrieves a file request from Dropbox. |
| [List File Requests](actions/list-file-requests.md) | GET | Retrieves file requests for the current user from Dropbox. |
| [Update File Request](actions/update-file-request.md) | PUT | Updates an existing file request in Dropbox. |

### File Revision

| Action | Method | Description |
| --- | --- | --- |
| [List File Revisions](actions/list-file-revisions.md) | GET | Retrieves revision history for a file from Dropbox. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Copy File or Folder](actions/copy-file-or-folder.md) | POST | Creates a copy of a file or folder in Dropbox. |
| [Create Shared Link](actions/create-shared-link.md) | POST | Creates a shared link in Dropbox, or returns an existing link. |
| [Delete File or Folder](actions/delete-file-or-folder.md) | DELETE | Deletes an existing file or folder from Dropbox. |
| [Move File or Folder](actions/move-file-or-folder.md) | PUT | Moves a file or folder in Dropbox. |
| [Restore File Revision](actions/restore-file-revision.md) | PUT | Restores a file revision in Dropbox. |
| [Revoke Shared Link](actions/revoke-shared-link.md) | DELETE | Deletes an existing shared link from Dropbox. |
| [Update Shared Link Settings](actions/update-shared-link-settings.md) | PUT | Updates shared link settings in Dropbox. |
| [Upload File](actions/upload-file.md) | POST | Uploads a new file to Dropbox. |

### Folder Cursor

| Action | Method | Description |
| --- | --- | --- |
| [Get Latest Folder Cursor](actions/get-latest-folder-cursor.md) | GET | Retrieves the latest cursor for a Dropbox folder. |

### Folder Entry

| Action | Method | Description |
| --- | --- | --- |
| [Continue Folder Listing](actions/continue-folder-listing.md) | GET | Retrieves more Dropbox folder contents using a cursor. |
| [List Folder Contents](actions/list-folder-contents.md) | GET | Retrieves the contents of a Dropbox folder. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Dropbox. |

### Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get File or Folder Metadata](actions/get-file-or-folder-metadata.md) | GET | Retrieves file or folder metadata from Dropbox. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Files and Folders](actions/search-files-and-folders.md) | GET | Finds files and folders in Dropbox by search query. |

### Shared Folder

| Action | Method | Description |
| --- | --- | --- |
| [List Shared Folders](actions/list-shared-folders.md) | GET | Retrieves shared folders for the current user from Dropbox. |

### Shared Folder Member

| Action | Method | Description |
| --- | --- | --- |
| [Add Shared Folder Members](actions/add-shared-folder-members.md) | POST | Adds members to a shared folder in Dropbox. |
| [List Shared Folder Members](actions/list-shared-folder-members.md) | GET | Retrieves members of a shared folder from Dropbox. |

### Shared Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Shared Link Metadata](actions/get-shared-link-metadata.md) | GET | Retrieves metadata for a Dropbox shared link. |
| [List Shared Links](actions/list-shared-links.md) | GET | Retrieves shared links for the current user from Dropbox. |

### Space Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Space Usage](actions/get-space-usage.md) | GET | Retrieves account space usage from Dropbox. |

### Temporary Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Temporary Link](actions/get-temporary-link.md) | GET | Retrieves a temporary download link from Dropbox. |

