# <img src="https://images.mindcloud.co/apps/icons/sharepoint-icon_1776192069750.png" alt="Microsoft SharePoint Online logo" width="28" height="28"> Microsoft SharePoint Online: Universal API

Access Microsoft SharePoint Online sites, document libraries, files, folders, lists, and list items through Microsoft Graph for organizational Microsoft 365 tenants.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/microsoftSharePointOnline/latest
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.microsoft.com/microsoft-365/sharepoint/collaboration
- **Vendor API docs:** https://learn.microsoft.com/en-us/graph/api/resources/sharepoint?view=graph-rest-1.0

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Root Site](actions/get-root-site.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftSharePointOnline/latest/actions/get-root-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Drive Items

| Action | Method | Description |
| --- | --- | --- |
| [Delete Drive Item](actions/delete-drive-item.md) | DELETE | Deletes a drive item from Microsoft SharePoint Online. |
| [Get Drive Item](actions/get-drive-item.md) | GET | Retrieves a drive item from Microsoft SharePoint Online. |
| [List Drive Root Items](actions/list-drive-root-items.md) | GET | Retrieves root drive items from Microsoft SharePoint Online. |
| [List Folder Items](actions/list-folder-items.md) | GET | Retrieves folder items from Microsoft SharePoint Online. |

### Drives

| Action | Method | Description |
| --- | --- | --- |
| [List Site Drives](actions/list-site-drives.md) | GET | Retrieves drives from a site in Microsoft SharePoint Online. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Download File](actions/download-file.md) | GET | Downloads a file from Microsoft SharePoint Online. |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Microsoft SharePoint Online. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a folder in Microsoft SharePoint Online. |

### List Items

| Action | Method | Description |
| --- | --- | --- |
| [Create List Item](actions/create-list-item.md) | POST | Creates a list item in Microsoft SharePoint Online. |
| [Delete List Item](actions/delete-list-item.md) | DELETE | Deletes a list item from Microsoft SharePoint Online. |
| [Get List Item](actions/get-list-item.md) | GET | Retrieves a list item from Microsoft SharePoint Online. |
| [List List Items](actions/list-list-items.md) | GET | Retrieves list items from Microsoft SharePoint Online. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Get List](actions/get-list.md) | GET | Retrieves a list from Microsoft SharePoint Online. |
| [List Site Lists](actions/list-site-lists.md) | GET | Retrieves lists from a site in Microsoft SharePoint Online. |

### Sites

| Action | Method | Description |
| --- | --- | --- |
| [Get Root Site](actions/get-root-site.md) | GET | Retrieves the root site from Microsoft SharePoint Online. |
| [Get Site](actions/get-site.md) | GET | Retrieves a site from Microsoft SharePoint Online. |
| [Search Sites](actions/search-sites.md) | GET | Finds sites in Microsoft SharePoint Online by keyword. |

