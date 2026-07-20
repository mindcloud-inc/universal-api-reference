# GatherContent: Native API Reference

A consolidated summary of GatherContent's API configuration and 42 documented operations, with links to official documentation.

- **Official docs:** https://docs.gathercontent.com/reference/introduction
- **API base URL:** `https://api.gathercontent.com`

## Authentication

### Basic Auth

Use your GatherContent login email as the username and your API key as the password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.gathercontent.com/reference/authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.gathercontent.v2+json` |

Responses from this API use JSON.

## Endpoints (42 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Alter Structure](actions/alter-structure.md) | `PUT /structures/:structure_uuid` | [docs](https://docs.gathercontent.com/reference/alterstructure) |
| [Apply Template To Item](actions/apply-template-to-item.md) | `POST /items/:item_id/apply_template` | [docs](https://docs.gathercontent.com/reference/applytemplate) |
| [Create Component](actions/create-component.md) | `POST /projects/:project_id/components` | [docs](https://docs.gathercontent.com/reference/createcomponent) |
| [Create Folder](actions/create-folder.md) | `POST /folders/:folder_uuid/folders` | [docs](https://docs.gathercontent.com/reference/createfolder) |
| [Create Item](actions/create-item.md) | `POST /projects/:project_id/items` | [docs](https://docs.gathercontent.com/reference/createitem) |
| [Create Template](actions/create-template.md) | `POST /projects/:project_id/templates` | [docs](https://docs.gathercontent.com/reference/createtemplate) |
| [Delete Component](actions/delete-component.md) | `DELETE /components/:component_uuid` | [docs](https://docs.gathercontent.com/reference/deletecomponent) |
| [Delete Files](actions/delete-files.md) | `DELETE /projects/:project_id/files` | [docs](https://docs.gathercontent.com/reference/deletefile) |
| [Delete Template](actions/delete-template.md) | `DELETE /templates/:template_id` | [docs](https://docs.gathercontent.com/reference/deletetemplate) |
| [Disconnect Template From Item](actions/disconnect-template-from-item.md) | `POST /items/:item_id/disconnect_template` | [docs](https://docs.gathercontent.com/reference/disconnecttemplate) |
| [Duplicate Item](actions/duplicate-item.md) | `POST /items/:item_id/duplicate` | [docs](https://docs.gathercontent.com/reference/duplicateitem) |
| [Duplicate Template](actions/duplicate-template.md) | `POST /templates/:template_id/duplicate` | [docs](https://docs.gathercontent.com/reference/duplicatetemplate) |
| [Get Component](actions/get-component.md) | `GET /components/:component_uuid` | [docs](https://docs.gathercontent.com/reference/getcomponent) |
| [Get Current User](actions/get-current-user.md) | `GET /me` | [docs](https://docs.gathercontent.com/reference/authentication) |
| [Get File](actions/get-file.md) | `GET /projects/:project_id/files/:file_id` | [docs](https://docs.gathercontent.com/reference/getfile) |
| [Get Item](actions/get-item.md) | `GET /items/:item_id` | [docs](https://docs.gathercontent.com/reference/getitem) |
| [Get Structure](actions/get-structure.md) | `GET /structures/:structure_uuid` | [docs](https://docs.gathercontent.com/reference/getstructure) |
| [Get Template](actions/get-template.md) | `GET /templates/:template_id` | [docs](https://docs.gathercontent.com/reference/gettemplate) |
| [List Components](actions/list-components.md) | `GET /projects/:project_id/components` | [docs](https://docs.gathercontent.com/reference/listcomponents) |
| [List Files](actions/list-files.md) | `GET /projects/:project_id/files` | [docs](https://docs.gathercontent.com/reference/listfiles) |
| [List Folder Tree](actions/list-folder-tree.md) | `GET /projects/:project_id/folders/tree` | [docs](https://docs.gathercontent.com/reference/listfoldersastree) |
| [List Folders](actions/list-folders.md) | `GET /projects/:project_id/folders` | [docs](https://docs.gathercontent.com/reference/listfolders) |
| [List Items](actions/list-items.md) | `GET /projects/:project_id/items` | [docs](https://docs.gathercontent.com/reference/listitems) |
| [List Projects](actions/list-projects.md) | `GET /v0.5/projects` | [docs](https://docs.gathercontent.com/reference/getprojects) |
| [List Templates](actions/list-templates.md) | `GET /projects/:project_id/templates` | [docs](https://docs.gathercontent.com/reference/listtemplates) |
| [List Webhooks](actions/list-webhooks.md) | `GET /projects/:project_id/webhooks` | [docs](https://docs.gathercontent.com/reference/listwebhooks-1) |
| [Move Folder](actions/move-folder.md) | `POST /folders/:folder_uuid/move` | [docs](https://docs.gathercontent.com/reference/movefolder) |
| [Move Item](actions/move-item.md) | `POST /items/:item_id/move` | [docs](https://docs.gathercontent.com/reference/moveitem) |
| [Rename Component](actions/rename-component.md) | `POST /components/:component_uuid/rename` | [docs](https://docs.gathercontent.com/reference/renamecomponent) |
| [Rename Folder](actions/rename-folder.md) | `POST /folders/:folder_uuid/rename` | [docs](https://docs.gathercontent.com/reference/renamefolder) |
| [Rename Item](actions/rename-item.md) | `POST /items/:item_id/rename` | [docs](https://docs.gathercontent.com/reference/renameitem) |
| [Rename Template](actions/rename-template.md) | `POST /templates/:template_id/rename` | [docs](https://docs.gathercontent.com/reference/renametemplate) |
| [Restore Folder](actions/restore-folder.md) | `POST /folders/:folder_uuid/restore` | [docs](https://docs.gathercontent.com/reference/restorefolder) |
| [Save Custom Structure As Template](actions/save-custom-structure-as-template.md) | `POST /items/:item_id/save_as_template` | [docs](https://docs.gathercontent.com/reference/savecustomstructureastemplate) |
| [Save Structure As Template](actions/save-structure-as-template.md) | `POST /structures/:structure_uuid/templates` | [docs](https://docs.gathercontent.com/reference/savestructureastemplate) |
| [Subscribe To Webhook Event](actions/subscribe-to-webhook-event.md) | `POST /projects/:project_id/webhooks/:event_name` | [docs](https://docs.gathercontent.com/reference/subscribetowebhook-1) |
| [Trash Or Delete Folder](actions/trash-or-delete-folder.md) | `DELETE /folders/:folder_uuid` | [docs](https://docs.gathercontent.com/reference/trashordeletefolder) |
| [Update Component Fields](actions/update-component-fields.md) | `PUT /components/:component_uuid/fields` | [docs](https://docs.gathercontent.com/reference/updatecomponentfields) |
| [Update Item Content](actions/update-item-content.md) | `POST /items/:item_id/content` | [docs](https://docs.gathercontent.com/reference/updateitemcontent) |
| [Update Item Structure](actions/update-item-structure.md) | `PUT /items/:item_id/structure` | [docs](https://docs.gathercontent.com/reference/updateitemstructure) |
| [Update Template Structure](actions/update-template-structure.md) | `PUT /templates/:template_id/structure` | [docs](https://docs.gathercontent.com/reference/updatetemplatestructure) |
| [Upload Files](actions/upload-files.md) | `POST /projects/:project_id/files` | [docs](https://docs.gathercontent.com/reference/upload-filed) |
