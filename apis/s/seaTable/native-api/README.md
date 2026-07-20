# SeaTable: Native API Reference

A consolidated summary of SeaTable's API configuration and 63 documented operations, with links to official documentation.

- **Official docs:** https://api.seatable.com/reference/introduction
- **API base URL:** `https://cloud.seatable.io`

## Authentication

### API Token

Use a SeaTable API token, plus the current base token and base UUID for base operations.

### Credentials

- **API Key:** `apiKey` · required
- **Base UUID:** `baseUuid` · required · The SeaTable base UUID returned by the base-token bootstrap call.
- **Base Token:** `baseToken` · required · The short-lived SeaTable base token used for base operations.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.seatable.com/reference/authentication)

## Endpoints (63 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Rows Into Big Data Backend](actions/add-rows-into-big-data-backend.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/add-archived-rows/` | [docs](https://api.seatable.com/reference/addbigdatarows) |
| [Add Single/Multiple Select Options](actions/add-single-multiple-select-options.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/column-options/` | [docs](https://api.seatable.com/reference/addselectoption-1) |
| [Append Columns](actions/append-columns.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/batch-append-columns/` | [docs](https://api.seatable.com/reference/appendcolumns-1) |
| [Append Rows](actions/append-rows.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/rows/` | [docs](https://api.seatable.com/reference/appendrows) |
| [Create Auto Links](actions/create-auto-links.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/auto-links/` | [docs](https://api.seatable.com/reference/autolinks) |
| [Create Row Links](actions/create-row-links.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/links/` | [docs](https://api.seatable.com/reference/createrowlink) |
| [Create Snapshot](actions/create-snapshot.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/snapshot/` | [docs](https://api.seatable.com/reference/createsnapshot) |
| [Create Table](actions/create-table.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/tables/` | [docs](https://api.seatable.com/reference/createtable) |
| [Create View](actions/create-view.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/views/` | [docs](https://api.seatable.com/reference/createview) |
| [Delete Base Asset](actions/delete-base-asset.md) | `DELETE /api/v2.1/dtable/app-asset/` | [docs](https://api.seatable.com/reference/deletebaseasset-2) |
| [Delete Base Asset In Custom Folder](actions/delete-base-asset-in-custom-folder.md) | `DELETE /api/v2.1/dtable/custom/app-asset-file/` | [docs](https://api.seatable.com/reference/deletebasecustomfolderasset-1) |
| [Delete Base Notifications](actions/delete-base-notifications.md) | `DELETE /api-gateway/api/v2/dtables/:base_uuid/notifications/` | [docs](https://api.seatable.com/reference/deletebasenotifications-1) |
| [Delete Column](actions/delete-column.md) | `DELETE /api-gateway/api/v2/dtables/:base_uuid/columns/` | [docs](https://api.seatable.com/reference/deletecolumn-1) |
| [Delete Comment](actions/delete-comment.md) | `DELETE /api-gateway/api/v2/dtables/:base_uuid/comments/:comment_id/` | [docs](https://api.seatable.com/reference/deletecomment) |
| [Delete Row Links](actions/delete-row-links.md) | `DELETE /api-gateway/api/v2/dtables/:base_uuid/links/` | [docs](https://api.seatable.com/reference/deleterowlink) |
| [Delete Rows](actions/delete-rows.md) | `DELETE /api-gateway/api/v2/dtables/:base_uuid/rows/` | [docs](https://api.seatable.com/reference/deleterow) |
| [Delete Single/Multiple Select Options](actions/delete-single-multiple-select-options.md) | `DELETE /api-gateway/api/v2/dtables/:base_uuid/column-options/` | [docs](https://api.seatable.com/reference/deleteselectoption-1) |
| [Delete Table](actions/delete-table.md) | `DELETE /api-gateway/api/v2/dtables/:base_uuid/tables/` | [docs](https://api.seatable.com/reference/deletetable) |
| [Delete View](actions/delete-view.md) | `DELETE /api-gateway/api/v2/dtables/:base_uuid/views/:view_name/` | [docs](https://api.seatable.com/reference/deleteview) |
| [Duplicate Table](actions/duplicate-table.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/tables/duplicate-table/` | [docs](https://api.seatable.com/reference/duplicatetable) |
| [Get Auto Link Task](actions/get-auto-link-task.md) | `GET /api-gateway/api/v2/dtables/:base_uuid/auto-link-task/` | [docs](https://api.seatable.com/reference/autolinktask) |
| [Get Base Activity Log](actions/get-base-activity-log.md) | `GET /api-gateway/api/v2/dtables/:base_uuid/operations/` | [docs](https://api.seatable.com/reference/getbaseactivitylog-1) |
| [Get Base Big Data Operations](actions/get-base-big-data-operations.md) | `GET /api-gateway/api/v2/dtables/:base_uuid/db-operations/` | [docs](https://api.seatable.com/reference/getbasebigdataoperations) |
| [Get Base Token With API Token](actions/get-base-token-with-api-token.md) | `GET /api/v2.1/dtable/app-access-token/` | [docs](https://api.seatable.com/reference/getbasetokenwithapitoken) |
| [Get Base Upload Link](actions/get-base-upload-link.md) | `GET /api/v2.1/dtable/app-upload-link/` | [docs](https://api.seatable.com/reference/getuploadlink) |
| [Get Comment](actions/get-comment.md) | `GET /api-gateway/api/v2/dtables/:base_uuid/comments/:comment_id/` | [docs](https://api.seatable.com/reference/getcomment) |
| [Get Custom Folder Download Link](actions/get-custom-folder-download-link.md) | `GET /api/v2.1/dtable/custom/app-download-link/` | [docs](https://api.seatable.com/reference/getcustomdownloadlink) |
| [Get Custom Folder Upload Link](actions/get-custom-folder-upload-link.md) | `GET /api/v2.1/dtable/custom/app-upload-link/` | [docs](https://api.seatable.com/reference/getcustomuploadlink) |
| [Get File Download Link](actions/get-file-download-link.md) | `GET /api/v2.1/dtable/app-download-link/` | [docs](https://api.seatable.com/reference/getfiledownloadlink) |
| [Get File Metadata](actions/get-file-metadata.md) | `GET /api/v2.1/dtable/custom/app-asset-file/` | [docs](https://api.seatable.com/reference/getcustomfilemetadata) |
| [Get Metadata](actions/get-metadata.md) | `GET /api-gateway/api/v2/dtables/:base_uuid/metadata/` | [docs](https://api.seatable.com/reference/getmetadata) |
| [Get Number of Comments](actions/get-number-of-comments.md) | `GET /api/v2.1/dtables/:base_uuid/rows-comments-num/` | [docs](https://api.seatable.com/reference/getnumberofcomments) |
| [Get Row](actions/get-row.md) | `GET /api-gateway/api/v2/dtables/:base_uuid/rows/:row_id/` | [docs](https://api.seatable.com/reference/getrow) |
| [Get Row Comments Count](actions/get-row-comments-count.md) | `GET /api-gateway/api/v2/dtables/:base_uuid/comments-count/` | [docs](https://api.seatable.com/reference/getrowcommentscount) |
| [Get View](actions/get-view.md) | `GET /api-gateway/api/v2/dtables/:base_uuid/views/:view_name/` | [docs](https://api.seatable.com/reference/getview) |
| [Insert Column](actions/insert-column.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/columns/` | [docs](https://api.seatable.com/reference/insertcolumn-1) |
| [List Base Notifications](actions/list-base-notifications.md) | `GET /api-gateway/api/v2/dtables/:base_uuid/notifications/` | [docs](https://api.seatable.com/reference/listbasenotifications-2) |
| [List Collaborators](actions/list-collaborators.md) | `GET /api-gateway/api/v2/dtables/:base_uuid/related-users/` | [docs](https://api.seatable.com/reference/listcollaborators) |
| [List Columns](actions/list-columns.md) | `GET /api-gateway/api/v2/dtables/:base_uuid/columns/` | [docs](https://api.seatable.com/reference/listcolumns-1) |
| [List Comments Within Days](actions/list-comments-within-days.md) | `GET /api-gateway/api/v2/dtables/:base_uuid/comments-within-days/` | [docs](https://api.seatable.com/reference/listcommentswithindays) |
| [List Files from Folder](actions/list-files-from-folder.md) | `GET /api/v2.1/dtable/custom/app-asset-dir/` | [docs](https://api.seatable.com/reference/getcustomfiles) |
| [List Row Activities](actions/list-row-activities.md) | `GET /api-gateway/api/v2/dtables/:base_uuid/activities/` | [docs](https://api.seatable.com/reference/listrowactivities-1) |
| [List Row Comments](actions/list-row-comments.md) | `GET /api-gateway/api/v2/dtables/:base_uuid/comments/` | [docs](https://api.seatable.com/reference/listrowcomments) |
| [List Row Links](actions/list-row-links.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/query-links/` | [docs](https://api.seatable.com/reference/listrowlinks) |
| [List Rows](actions/list-rows.md) | `GET /api-gateway/api/v2/dtables/:base_uuid/rows/` | [docs](https://api.seatable.com/reference/listrows) |
| [List Views](actions/list-views.md) | `GET /api-gateway/api/v2/dtables/:base_uuid/views/` | [docs](https://api.seatable.com/reference/listviews) |
| [Lock Rows](actions/lock-rows.md) | `PUT /api-gateway/api/v2/dtables/:base_uuid/lock-rows/` | [docs](https://api.seatable.com/reference/lockrows) |
| [Mark Base Notifications as Seen](actions/mark-base-notifications-as-seen.md) | `PUT /api-gateway/api/v2/dtables/:base_uuid/notifications/` | [docs](https://api.seatable.com/reference/markbasenotificationsasseen-1) |
| [Mark Notification Read/Unread](actions/mark-notification-read-unread.md) | `PUT /api-gateway/api/v2/dtables/:base_uuid/notifications/:notification_id/` | [docs](https://api.seatable.com/reference/markbasenotificationasseen-1) |
| [Move Rows To Big Data Backend](actions/move-rows-to-big-data-backend.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/archive-view/` | [docs](https://api.seatable.com/reference/moverowstobigdata) |
| [Move Rows To Normal Backend](actions/move-rows-to-normal-backend.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/unarchive/` | [docs](https://api.seatable.com/reference/moverowstonormalbackend) |
| [Query SeaTable With SQL](actions/query-seatable-with-sql.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/sql/` | [docs](https://api.seatable.com/reference/querysql) |
| [Rename Table](actions/rename-table.md) | `PUT /api-gateway/api/v2/dtables/:base_uuid/tables/` | [docs](https://api.seatable.com/reference/renametable) |
| [Restore Big Data Operations](actions/restore-big-data-operations.md) | `PUT /api-gateway/api/v2/dtables/:base_uuid/restore-operations/:op_id/` | [docs](https://api.seatable.com/reference/restorebigdataoperations) |
| [Send Toast Notification](actions/send-toast-notification.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/ui-toasts/` | [docs](https://api.seatable.com/reference/sendtoastnotification-1) |
| [Unlock Rows](actions/unlock-rows.md) | `PUT /api-gateway/api/v2/dtables/:base_uuid/unlock-rows/` | [docs](https://api.seatable.com/reference/unlockrows) |
| [Update Column](actions/update-column.md) | `PUT /api-gateway/api/v2/dtables/:base_uuid/columns/` | [docs](https://api.seatable.com/reference/updatecolumn-1) |
| [Update Column Cascade Settings](actions/update-column-cascade-settings.md) | `POST /api-gateway/api/v2/dtables/:base_uuid/column-cascade-settings/` | [docs](https://api.seatable.com/reference/updatecolumncascade-1) |
| [Update Row Links](actions/update-row-links.md) | `PUT /api-gateway/api/v2/dtables/:base_uuid/links/` | [docs](https://api.seatable.com/reference/updaterowlink) |
| [Update Rows](actions/update-rows.md) | `PUT /api-gateway/api/v2/dtables/:base_uuid/rows/` | [docs](https://api.seatable.com/reference/updaterow) |
| [Update Single/Multiple Select Options](actions/update-single-multiple-select-options.md) | `PUT /api-gateway/api/v2/dtables/:base_uuid/column-options/` | [docs](https://api.seatable.com/reference/updateselectoption-1) |
| [Update View](actions/update-view.md) | `PUT /api-gateway/api/v2/dtables/:base_uuid/views/:view_name/` | [docs](https://api.seatable.com/reference/updateview) |
| [Upload File Or Image](actions/upload-file-or-image.md) | `POST /seafhttp/upload-api/:upload_link?ret-json=1` | [docs](https://api.seatable.com/reference/uploadfile) |
