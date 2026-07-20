# <img src="https://images.mindcloud.co/apps/icons/hidrive_1776791956264.png" alt="HiDrive logo" width="28" height="28"> HiDrive: Universal API

HiDrive is STRATO's cloud storage service for managing files, folders, shares, uploads, snapshots, and account storage features through the HiDrive HTTP API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hidrive/latest
- **Category:** Content & Files / Storage
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.strato.de/cloud-speicher/hidrive/
- **Vendor API docs:** https://developer.hidrive.com/http-api-reference/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get App Info](actions/get-app-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hidrive/latest/actions/get-app-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### App Info

| Action | Method | Description |
| --- | --- | --- |
| [Get App Info](actions/get-app-info.md) | GET | Retrieves app information from HiDrive. |

### Disabled Status

| Action | Method | Description |
| --- | --- | --- |
| [Get Disabled Status](actions/get-disabled-status.md) | GET | Retrieves the disabled status from HiDrive. |

### Feature

| Action | Method | Description |
| --- | --- | --- |
| [Get Features](actions/get-features.md) | GET | Retrieves feature information from HiDrive. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Copy File](actions/copy-file.md) | POST | Copies a file in HiDrive. |
| [Delete File](actions/delete-file.md) | DELETE | Deletes a file from HiDrive. |
| [Move File](actions/move-file.md) | PUT | Moves a file in HiDrive. |
| [Rename File](actions/rename-file.md) | PUT | Renames a file in HiDrive. |

### File Download Url

| Action | Method | Description |
| --- | --- | --- |
| [Get File Download URL](actions/get-file-download-url.md) | GET | Retrieves a file download URL from HiDrive. |

### File Hash

| Action | Method | Description |
| --- | --- | --- |
| [Get File Hashes](actions/get-file-hashes.md) | GET | Retrieves file hashes from HiDrive. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Copy Directory](actions/copy-directory.md) | POST | Copies a directory in HiDrive. |
| [Create Directory](actions/create-directory.md) | POST | Creates a new directory in HiDrive. |
| [Delete Directory](actions/delete-directory.md) | DELETE | Deletes a directory from HiDrive. |
| [List Directory](actions/list-directory.md) | GET | Retrieves a directory from HiDrive. |
| [List Home Directory](actions/list-home-directory.md) | GET | Retrieves the home directory from HiDrive. |
| [Move Directory](actions/move-directory.md) | PUT | Moves a directory in HiDrive. |
| [Rename Directory](actions/rename-directory.md) | PUT | Renames a directory in HiDrive. |

### Mail Upload

| Action | Method | Description |
| --- | --- | --- |
| [Create Mail Upload](actions/create-mail-upload.md) | POST | Creates a new mail upload in HiDrive. |
| [Delete Mail Upload](actions/delete-mail-upload.md) | DELETE | Deletes a mail upload from HiDrive. |
| [List Mail Uploads](actions/list-mail-uploads.md) | GET | Retrieves mail uploads from HiDrive. |
| [Update Mail Upload](actions/update-mail-upload.md) | PUT | Updates an existing mail upload in HiDrive. |

### Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Metadata](actions/get-metadata.md) | GET | Retrieves file metadata from HiDrive. |
| [Update Metadata](actions/update-metadata.md) | PUT | Updates file metadata in HiDrive. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Files](actions/search-files.md) | GET | Finds files in HiDrive by search query. |

### Share

| Action | Method | Description |
| --- | --- | --- |
| [Create Share](actions/create-share.md) | POST | Creates a new share in HiDrive. |
| [Delete Share](actions/delete-share.md) | DELETE | Deletes a share from HiDrive. |
| [Get Share Info](actions/get-share-info.md) | GET | Retrieves share information from HiDrive. |
| [List Shares](actions/list-shares.md) | GET | Retrieves shares from HiDrive. |
| [Update Share](actions/update-share.md) | PUT | Updates an existing share in HiDrive. |

### Share Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Share Link](actions/create-share-link.md) | POST | Creates a new share link in HiDrive. |
| [Delete Share Link](actions/delete-share-link.md) | DELETE | Deletes a share link from HiDrive. |
| [Get Share Link Info](actions/get-share-link-info.md) | GET | Retrieves share link information from HiDrive. |
| [List Share Links](actions/list-share-links.md) | GET | Retrieves share links from HiDrive. |
| [Update Share Link](actions/update-share-link.md) | PUT | Updates an existing share link in HiDrive. |

### Share Upload

| Action | Method | Description |
| --- | --- | --- |
| [Create Share Upload](actions/create-share-upload.md) | POST | Creates a new share upload in HiDrive. |
| [Delete Share Upload](actions/delete-share-upload.md) | DELETE | Deletes a share upload from HiDrive. |
| [List Share Uploads](actions/list-share-uploads.md) | GET | Retrieves share uploads from HiDrive. |
| [Update Share Upload](actions/update-share-upload.md) | PUT | Updates an existing share upload in HiDrive. |

### Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [List Snapshots](actions/list-snapshots.md) | GET | Retrieves snapshots from HiDrive. |

### Unique Identifier

| Action | Method | Description |
| --- | --- | --- |
| [Get Unique Identifier](actions/get-unique-identifier.md) | GET | Retrieves a unique identifier from HiDrive. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from HiDrive. |

