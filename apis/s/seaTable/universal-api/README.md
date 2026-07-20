# <img src="https://images.mindcloud.co/apps/icons/sea-table_1774026796548.png" alt="SeaTable logo" width="28" height="28"> SeaTable: Universal API

Manage SeaTable bases, records, views, columns, files, and snapshots

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/seaTable/latest
- **Category:** IT Operations / Database
- **Actions:** 63
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://seatable.com
- **Vendor API docs:** https://api.seatable.com/reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Base Token With API Token](actions/get-base-token-with-api-token.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaTable/latest/actions/get-base-token-with-api-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (63)

### A Base Asset

| Action | Method | Description |
| --- | --- | --- |
| [Delete Base Asset](actions/delete-base-asset.md) | DELETE | Deletes an asset from a SeaTable base. |

### Auto Link Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Auto Links](actions/create-auto-links.md) | POST | Creates automatic row links in a SeaTable base. |
| [Get Auto Link Task](actions/get-auto-link-task.md) | GET | Retrieves an auto link task from SeaTable. |

### Base Activity Log

| Action | Method | Description |
| --- | --- | --- |
| [Get Base Activity Log](actions/get-base-activity-log.md) | GET | Retrieves the activity log for a SeaTable base. |

### Base Asset

| Action | Method | Description |
| --- | --- | --- |
| [Get File Download Link](actions/get-file-download-link.md) | GET | Retrieves a download link for a SeaTable file. |
| [Upload File Or Image](actions/upload-file-or-image.md) | POST | Uploads a file or image to SeaTable. |

### Base Big Data Operations

| Action | Method | Description |
| --- | --- | --- |
| [Get Base Big Data Operations](actions/get-base-big-data-operations.md) | GET | Retrieves big data operations for a SeaTable base. |

### Base Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Metadata](actions/get-metadata.md) | GET | Retrieves metadata for a SeaTable base. |

### Base Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Delete Base Notifications](actions/delete-base-notifications.md) | DELETE | Deletes notifications from a SeaTable base. |
| [List Base Notifications](actions/list-base-notifications.md) | GET | Lists notifications for a SeaTable base. |

### Base Notifications As Seen

| Action | Method | Description |
| --- | --- | --- |
| [Mark Base Notifications as Seen](actions/mark-base-notifications-as-seen.md) | PUT | Marks all notifications as seen in a SeaTable base. |

### Base Token

| Action | Method | Description |
| --- | --- | --- |
| [Get Base Token With API Token](actions/get-base-token-with-api-token.md) | GET | Retrieves a SeaTable base token with an API token. |

### Base Upload Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Base Upload Link](actions/get-base-upload-link.md) | GET | Retrieves an upload link for a SeaTable base asset. |

### Big Data Operations

| Action | Method | Description |
| --- | --- | --- |
| [Restore Big Data Operations](actions/restore-big-data-operations.md) | PUT | Restores big data operations in a SeaTable base. |

### Big Data Row

| Action | Method | Description |
| --- | --- | --- |
| [Move Rows To Normal Backend](actions/move-rows-to-normal-backend.md) | PUT | Moves rows back to a SeaTable normal backend. |

### Collaborator

| Action | Method | Description |
| --- | --- | --- |
| [List Collaborators](actions/list-collaborators.md) | GET | Lists collaborators for a SeaTable base. |

### Column

| Action | Method | Description |
| --- | --- | --- |
| [Append Columns](actions/append-columns.md) | POST | Creates multiple columns in a SeaTable base. |
| [Delete Column](actions/delete-column.md) | DELETE | Deletes a column from a SeaTable base. |
| [Insert Column](actions/insert-column.md) | POST | Creates a column in a SeaTable base. |
| [List Columns](actions/list-columns.md) | GET | Lists columns in a SeaTable base. |
| [Update Column](actions/update-column.md) | PUT | Updates a column in a SeaTable base. |

### Column Cascade Setting

| Action | Method | Description |
| --- | --- | --- |
| [Update Column Cascade Settings](actions/update-column-cascade-settings.md) | PUT | Updates column cascade settings in a SeaTable base. |

### Comments Within Days

| Action | Method | Description |
| --- | --- | --- |
| [List Comments Within Days](actions/list-comments-within-days.md) | GET | Lists comments from a SeaTable base within specific days. |

### File Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get File Metadata](actions/get-file-metadata.md) | GET | Retrieves metadata for a file in a SeaTable custom folder. |

### Files From Folder

| Action | Method | Description |
| --- | --- | --- |
| [List Files from Folder](actions/list-files-from-folder.md) | GET | Lists files from a SeaTable custom folder. |

### Folder File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Base Asset In Custom Folder](actions/delete-base-asset-in-custom-folder.md) | DELETE | Deletes an asset from a SeaTable custom folder. |
| [Get Custom Folder Download Link](actions/get-custom-folder-download-link.md) | GET | Retrieves a download link for a SeaTable custom folder. |

### Folder Upload Link

| Action | Method | Description |
| --- | --- | --- |
| [Get Custom Folder Upload Link](actions/get-custom-folder-upload-link.md) | GET | Retrieves an upload link for a SeaTable custom folder. |

### Notification Read/unread

| Action | Method | Description |
| --- | --- | --- |
| [Mark Notification Read/Unread](actions/mark-notification-read-unread.md) | PUT | Marks a SeaTable notification as read or unread. |

### Number Of Comments

| Action | Method | Description |
| --- | --- | --- |
| [Get Number of Comments](actions/get-number-of-comments.md) | GET | Retrieves the number of comments in a SeaTable base. |

### Row

| Action | Method | Description |
| --- | --- | --- |
| [Append Rows](actions/append-rows.md) | POST | Creates rows in a SeaTable base. |
| [Delete Rows](actions/delete-rows.md) | DELETE | Deletes rows from a SeaTable base. |
| [Get Row](actions/get-row.md) | GET | Retrieves a row from a SeaTable base. |
| [List Rows](actions/list-rows.md) | GET | Lists rows from a SeaTable base. |
| [Update Rows](actions/update-rows.md) | PUT | Updates rows in a SeaTable base. |

### Row Activities

| Action | Method | Description |
| --- | --- | --- |
| [List Row Activities](actions/list-row-activities.md) | GET | Lists row activities in a SeaTable base. |

### Row Comment

| Action | Method | Description |
| --- | --- | --- |
| [Delete Comment](actions/delete-comment.md) | DELETE | Deletes a comment from a SeaTable base. |
| [Get Comment](actions/get-comment.md) | GET | Retrieves a comment from a SeaTable base. |
| [List Row Comments](actions/list-row-comments.md) | GET | Lists row comments in a SeaTable base. |

### Row Comment Count

| Action | Method | Description |
| --- | --- | --- |
| [Get Row Comments Count](actions/get-row-comments-count.md) | GET | Retrieves the row comment count for a SeaTable base. |

### Row Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Row Links](actions/create-row-links.md) | POST | Creates row links in a SeaTable base. |
| [Delete Row Links](actions/delete-row-links.md) | DELETE | Deletes row links from a SeaTable base. |
| [List Row Links](actions/list-row-links.md) | GET | Lists row links in a SeaTable base. |
| [Update Row Links](actions/update-row-links.md) | PUT | Updates row links in a SeaTable base. |

### Row Lock

| Action | Method | Description |
| --- | --- | --- |
| [Lock Rows](actions/lock-rows.md) | PUT | Locks rows in a SeaTable base. |
| [Unlock Rows](actions/unlock-rows.md) | PUT | Unlocks rows in a SeaTable base. |

### Rows Into Big Data Backend

| Action | Method | Description |
| --- | --- | --- |
| [Add Rows Into Big Data Backend](actions/add-rows-into-big-data-backend.md) | POST | Adds rows to a SeaTable big data backend. |

### Rows To Big Data Backend

| Action | Method | Description |
| --- | --- | --- |
| [Move Rows To Big Data Backend](actions/move-rows-to-big-data-backend.md) | PUT | Moves rows to a SeaTable big data backend. |

### Select Option

| Action | Method | Description |
| --- | --- | --- |
| [Add Single/Multiple Select Options](actions/add-single-multiple-select-options.md) | POST | Creates single or multiple select options in SeaTable. |
| [Delete Single/Multiple Select Options](actions/delete-single-multiple-select-options.md) | DELETE | Deletes single or multiple select options from SeaTable. |
| [Update Single/Multiple Select Options](actions/update-single-multiple-select-options.md) | PUT | Updates single or multiple select options in SeaTable. |

### Snapshot

| Action | Method | Description |
| --- | --- | --- |
| [Create Snapshot](actions/create-snapshot.md) | POST | Creates a snapshot of a SeaTable base. |

### Sql Query Result

| Action | Method | Description |
| --- | --- | --- |
| [Query SeaTable With SQL](actions/query-seatable-with-sql.md) | GET | Queries a SeaTable base with SQL. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Create Table](actions/create-table.md) | POST | Creates a table in a SeaTable base. |
| [Delete Table](actions/delete-table.md) | DELETE | Deletes a table from a SeaTable base. |
| [Duplicate Table](actions/duplicate-table.md) | POST | Duplicates a table in a SeaTable base. |
| [Rename Table](actions/rename-table.md) | PUT | Renames a table in a SeaTable base. |

### Toast Notification

| Action | Method | Description |
| --- | --- | --- |
| [Send Toast Notification](actions/send-toast-notification.md) | POST | Sends a toast notification in a SeaTable base. |

### View

| Action | Method | Description |
| --- | --- | --- |
| [Create View](actions/create-view.md) | POST | Creates a view in a SeaTable base. |
| [Delete View](actions/delete-view.md) | DELETE | Deletes a view from a SeaTable base. |
| [Get View](actions/get-view.md) | GET | Retrieves a view from a SeaTable base. |
| [List Views](actions/list-views.md) | GET | Lists views in a SeaTable base. |
| [Update View](actions/update-view.md) | PUT | Updates a view in a SeaTable base. |

