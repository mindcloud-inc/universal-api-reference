# <img src="https://images.mindcloud.co/apps/icons/m-sshare-point_1776192578963.png" alt="MS SharePoint logo" width="28" height="28"> MS SharePoint: Universal API

Connect to SharePoint sites, lists, drives, files, and permissions through Microsoft Graph.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mSSharePoint/latest
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.microsoft.com/microsoft-365/sharepoint/collaboration
- **Vendor API docs:** https://learn.microsoft.com/en-us/graph/api/resources/sharepoint?view=graph-rest-1.0

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Root Site](actions/get-root-site.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mSSharePoint/latest/actions/get-root-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Columns

| Action | Method | Description |
| --- | --- | --- |
| [List List Columns](actions/list-list-columns.md) | GET | Retrieves columns from a SharePoint list. |

### Drive Items

| Action | Method | Description |
| --- | --- | --- |
| [Delete Drive Item](actions/delete-drive-item.md) | DELETE | Deletes a SharePoint drive item. |
| [Get Drive Item](actions/get-drive-item.md) | GET | Retrieves a SharePoint drive item. |
| [List Drive Root Items](actions/list-drive-root-items.md) | GET | Retrieves items from a SharePoint drive root folder. |
| [List Folder Items](actions/list-folder-items.md) | GET | Retrieves items from a SharePoint folder. |
| [Search Drive Items](actions/search-drive-items.md) | GET | Finds drive items in SharePoint by search term. |

### Drives

| Action | Method | Description |
| --- | --- | --- |
| [Get Drive](actions/get-drive.md) | GET | Retrieves a SharePoint drive. |
| [List Site Drives](actions/list-site-drives.md) | GET | Retrieves drives for a SharePoint site. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Downloads a file from SharePoint. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to SharePoint. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in SharePoint. |

### List Item Fields

| Action | Method | Description |
| --- | --- | --- |
| [Get List Item Fields](actions/get-list-item-fields.md) | GET | Retrieves field values for a SharePoint list item. |

### List Items

| Action | Method | Description |
| --- | --- | --- |
| [Create List Item](actions/create-list-item.md) | POST | Creates a new item in a SharePoint list. |
| [Delete List Item](actions/delete-list-item.md) | DELETE | Deletes an item from a SharePoint list. |
| [Get List Item](actions/get-list-item.md) | GET | Retrieves a SharePoint list item. |
| [List List Items](actions/list-list-items.md) | GET | Retrieves items from a SharePoint list. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Get List](actions/get-list.md) | GET | Retrieves a SharePoint list. |
| [List Site Lists](actions/list-site-lists.md) | GET | Retrieves lists for a SharePoint site. |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [List Drive Item Permissions](actions/list-drive-item-permissions.md) | GET | Retrieves permissions for a SharePoint drive item. |

### Sites

| Action | Method | Description |
| --- | --- | --- |
| [Get Root Site](actions/get-root-site.md) | GET | Retrieves the root SharePoint site. |
| [Get Site](actions/get-site.md) | GET | Retrieves a SharePoint site. |
| [Get Site By Path](actions/get-site-by-path.md) | GET | Retrieves a SharePoint site by path. |
| [List Subsites](actions/list-subsites.md) | GET | Retrieves subsites for a SharePoint site. |
| [Search Sites](actions/search-sites.md) | GET | Finds SharePoint sites by search term. |

