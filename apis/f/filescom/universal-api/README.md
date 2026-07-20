# <img src="https://images.mindcloud.co/apps/icons/images-12_1774552937346.png" alt="Files.com logo" width="28" height="28"> Files.com: Universal API

Store files, manage folders, automate transfers, and orchestrate secure file operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/filescom/latest
- **Category:** Content & Files / Storage
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.files.com/
- **Vendor API docs:** https://www.files.com/docs/sdk-and-apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Site](actions/get-site.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filescom/latest/actions/get-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Automation

| Action | Method | Description |
| --- | --- | --- |
| [Get Automation](actions/get-automation.md) | GET | Finds an automation in Files.com by ID. |
| [List Automations](actions/list-automations.md) | GET | Retrieves automations from a Files.com site. |
| [Run Automation Now](actions/run-automation-now.md) | PUT | Manually runs an automation in Files.com. |

### Bundle

| Action | Method | Description |
| --- | --- | --- |
| [Get Bundle](actions/get-bundle.md) | GET | Finds a share link in Files.com by ID. |
| [List Bundles](actions/list-bundles.md) | GET | Retrieves share links from a Files.com site. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Begin File Upload](actions/begin-file-upload.md) | POST | Begins a file upload in Files.com. |
| [Copy File or Folder](actions/copy-file-or-folder.md) | POST | Copies a file or folder within Files.com. |
| [Delete File or Folder](actions/delete-file-or-folder.md) | DELETE | Deletes a file or folder from Files.com. |
| [Get File Download Link](actions/get-file-download-link.md) | GET | Retrieves a file download link from Files.com. |
| [Get File or Folder Metadata](actions/get-file-or-folder-metadata.md) | GET | Finds a file or folder in Files.com by path. |
| [Update File or Folder Metadata](actions/update-file-or-folder-metadata.md) | PUT | Updates file or folder metadata in Files.com. |

### File Action

| Action | Method | Description |
| --- | --- | --- |
| [Move File or Folder](actions/move-file-or-folder.md) | PUT | Moves a file or folder within Files.com. |

### File Comment

| Action | Method | Description |
| --- | --- | --- |
| [List File Comments](actions/list-file-comments.md) | GET | Retrieves file comments by path from Files.com. |

### File History

| Action | Method | Description |
| --- | --- | --- |
| [List File History](actions/list-file-history.md) | GET | Retrieves history for a file from Files.com. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Files.com. |
| [List Folder Contents](actions/list-folder-contents.md) | GET | Retrieves folder contents by path from Files.com. |

### Folder History

| Action | Method | Description |
| --- | --- | --- |
| [List Folder History](actions/list-folder-history.md) | GET | Retrieves history for a folder from Files.com. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Get Group](actions/get-group.md) | GET | Finds a group in Files.com by ID. |
| [List Groups](actions/list-groups.md) | GET | Retrieves group records from a Files.com site. |

### History Event

| Action | Method | Description |
| --- | --- | --- |
| [List History](actions/list-history.md) | GET | Retrieves site action history from Files.com. |

### Login History

| Action | Method | Description |
| --- | --- | --- |
| [List Login History](actions/list-login-history.md) | GET | Retrieves site login history from Files.com. |

### Notification

| Action | Method | Description |
| --- | --- | --- |
| [Get Notification](actions/get-notification.md) | GET | Finds a notification in Files.com by ID. |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notifications from a Files.com site. |

### Permission

| Action | Method | Description |
| --- | --- | --- |
| [List Permissions](actions/list-permissions.md) | GET | Retrieves permission records from a Files.com site. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Finds a project in Files.com by ID. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from a Files.com site. |

### Request

| Action | Method | Description |
| --- | --- | --- |
| [List Requests](actions/list-requests.md) | GET | Retrieves requests from a Files.com site. |
| [List Requests by Folder Path](actions/list-requests-by-folder-path.md) | GET | Retrieves requests for a folder path from Files.com. |

### Site

| Action | Method | Description |
| --- | --- | --- |
| [Get Site](actions/get-site.md) | GET | Retrieves current site settings from Files.com. |

### Site Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Site Usage](actions/get-site-usage.md) | GET | Retrieves site usage data from Files.com. |

### Sync

| Action | Method | Description |
| --- | --- | --- |
| [Get Sync](actions/get-sync.md) | GET | Finds a sync in Files.com by ID. |
| [List Syncs](actions/list-syncs.md) | GET | Retrieves syncs from a Files.com site. |
| [Run Sync Now](actions/run-sync-now.md) | PUT | Manually runs a sync in Files.com. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Finds a user in Files.com by ID. |
| [List Users](actions/list-users.md) | GET | Retrieves user accounts from a Files.com site. |

### User History

| Action | Method | Description |
| --- | --- | --- |
| [List User History](actions/list-user-history.md) | GET | Retrieves history for a user from Files.com. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Finds a workspace in Files.com by ID. |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves workspaces from a Files.com site. |

