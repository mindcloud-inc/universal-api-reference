# <img src="https://images.mindcloud.co/apps/icons/pixxio_1776097746369.png" alt="pixx.io logo" width="28" height="28"> pixx.io: Universal API

Digital asset management and media storage platform for files, folders, collections, shares, metadata, users, and permissions.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pixxio/latest
- **Category:** Content & Files / Storage
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pixx.io
- **Vendor API docs:** https://api.pixxio.com/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pixxio/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in your pixx.io workspace. |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a collection from your pixx.io workspace. |
| [List Collections](actions/list-collections.md) | GET | Retrieves collections from your pixx.io workspace. |

### Custom Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Metadata](actions/get-custom-metadata.md) | GET | Retrieves a custom metadata field from your pixx.io workspace. |
| [List Custom Metadata](actions/list-custom-metadata.md) | GET | Retrieves custom metadata fields from your pixx.io workspace. |

### Direct Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Direct Link](actions/create-direct-link.md) | POST | Creates a new direct link in your pixx.io workspace. |
| [Get Direct Link](actions/get-direct-link.md) | GET | Retrieves a direct link from your pixx.io workspace. |
| [List Direct Links](actions/list-direct-links.md) | GET | Retrieves direct links from your pixx.io workspace. |

### Directory

| Action | Method | Description |
| --- | --- | --- |
| [Get Directory](actions/get-directory.md) | GET | Retrieves a directory from your pixx.io workspace. |
| [List Directories](actions/list-directories.md) | GET | Retrieves directories from your pixx.io workspace. |
| [List Directory Tree](actions/list-directory-tree.md) | GET | Retrieves the directory tree from your pixx.io workspace. |

### External Share

| Action | Method | Description |
| --- | --- | --- |
| [Create External Share](actions/create-external-share.md) | POST | Creates a new external share in your pixx.io workspace. |
| [Get External Share](actions/get-external-share.md) | GET | Retrieves an external share from your pixx.io workspace. |
| [List External Shares](actions/list-external-shares.md) | GET | Retrieves external shares from your pixx.io workspace. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Downloads a converted file from your pixx.io workspace. |
| [Download Files](actions/download-files.md) | GET | Downloads converted files from your pixx.io workspace. |
| [Get File](actions/get-file.md) | GET | Retrieves a file from your pixx.io workspace. |
| [List Files](actions/list-files.md) | GET | Retrieves files from your pixx.io workspace. |

### File State

| Action | Method | Description |
| --- | --- | --- |
| [Get File State](actions/get-file-state.md) | GET | Retrieves a file state from your pixx.io workspace. |
| [List File States](actions/list-file-states.md) | GET | Retrieves file states from your pixx.io workspace. |

### Important Metadata

| Action | Method | Description |
| --- | --- | --- |
| [List Important Metadata](actions/list-important-metadata.md) | GET | Retrieves important metadata from your pixx.io workspace. |

### Internal Metadata

| Action | Method | Description |
| --- | --- | --- |
| [List Internal Metadata](actions/list-internal-metadata.md) | GET | Retrieves internal metadata from your pixx.io workspace. |

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Job](actions/get-job.md) | GET | Retrieves a job from your pixx.io workspace. |

### Keyword

| Action | Method | Description |
| --- | --- | --- |
| [Download Keywords CSV](actions/download-keywords-csv.md) | GET | Downloads keywords as a CSV from your pixx.io workspace. |
| [List Keywords](actions/list-keywords.md) | GET | Retrieves keywords from your pixx.io workspace. |

### Permission Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Permission Group](actions/get-permission-group.md) | GET | Retrieves a permission group from your pixx.io workspace. |
| [List Permission Groups](actions/list-permission-groups.md) | GET | Retrieves permission groups from your pixx.io workspace. |

### Portal

| Action | Method | Description |
| --- | --- | --- |
| [List Portals](actions/list-portals.md) | GET | Retrieves portals from your pixx.io workspace. |

### Standard Metadata

| Action | Method | Description |
| --- | --- | --- |
| [List Standard Metadata](actions/list-standard-metadata.md) | GET | Retrieves standard metadata from your pixx.io workspace. |

### Synonym

| Action | Method | Description |
| --- | --- | --- |
| [Download Synonyms CSV](actions/download-synonyms-csv.md) | GET | Downloads synonyms as a CSV from your pixx.io workspace. |
| [List Synonyms](actions/list-synonyms.md) | GET | Retrieves synonyms from your pixx.io workspace. |

### Synonym Column

| Action | Method | Description |
| --- | --- | --- |
| [List Synonym Columns](actions/list-synonym-columns.md) | GET | Retrieves synonym columns from your pixx.io workspace. |

### Upload Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Upload Link](actions/create-upload-link.md) | POST | Creates a new upload link in your pixx.io workspace. |
| [Get Upload Link](actions/get-upload-link.md) | GET | Retrieves an upload link from your pixx.io workspace. |
| [Get Upload Link Basic Info](actions/get-upload-link-basic-info.md) | GET | Retrieves basic upload link info from your pixx.io workspace. |
| [List Upload Links](actions/list-upload-links.md) | GET | Retrieves upload links from your pixx.io workspace. |

### Upload Link User

| Action | Method | Description |
| --- | --- | --- |
| [List Upload Link Users](actions/list-upload-link-users.md) | GET | Retrieves upload link users from your pixx.io workspace. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from your pixx.io workspace. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from your pixx.io workspace. |
| [List Users](actions/list-users.md) | GET | Retrieves users from your pixx.io workspace. |

