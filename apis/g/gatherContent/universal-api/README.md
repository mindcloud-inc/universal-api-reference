# <img src="https://images.mindcloud.co/apps/icons/gathercontent-icon_1776100606435.png" alt="GatherContent logo" width="28" height="28"> GatherContent: Universal API

GatherContent is a content operations platform API for managing projects, items, templates, folders, files, and webhooks through REST endpoints.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gatherContent/latest
- **Category:** Website & App Building / CMS
- **Actions:** 42
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gathercontent.com
- **Vendor API docs:** https://docs.gathercontent.com/reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gatherContent/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (42)

### Component

| Action | Method | Description |
| --- | --- | --- |
| [Create Component](actions/create-component.md) | POST | Creates a new component in GatherContent. |
| [Delete Component](actions/delete-component.md) | DELETE | Deletes an existing component from GatherContent. |
| [Get Component](actions/get-component.md) | GET | Retrieves a component from GatherContent. |
| [List Components](actions/list-components.md) | GET | Lists components in a GatherContent project. |
| [Rename Component](actions/rename-component.md) | PUT | Renames an existing component in GatherContent. |
| [Update Component Fields](actions/update-component-fields.md) | PUT | Updates fields for an existing component in GatherContent. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Files](actions/delete-files.md) | DELETE | Deletes files from a GatherContent project. |
| [Get File](actions/get-file.md) | GET | Retrieves a file from GatherContent. |
| [List Files](actions/list-files.md) | GET | Lists files in a GatherContent project. |
| [Upload Files](actions/upload-files.md) | POST | Uploads a file to a GatherContent project. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in GatherContent. |
| [List Folders](actions/list-folders.md) | GET | Lists folders in a GatherContent project. |
| [Move Folder](actions/move-folder.md) | PUT | Moves an existing folder in GatherContent. |
| [Rename Folder](actions/rename-folder.md) | PUT | Renames an existing folder in GatherContent. |
| [Restore Folder](actions/restore-folder.md) | PUT | Restores a trashed folder in GatherContent. |
| [Trash Or Delete Folder](actions/trash-or-delete-folder.md) | DELETE | Trashes or permanently deletes a folder in GatherContent. |

### Folder Tree

| Action | Method | Description |
| --- | --- | --- |
| [List Folder Tree](actions/list-folder-tree.md) | GET | Lists folders in a GatherContent project tree. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Apply Template To Item](actions/apply-template-to-item.md) | PUT | Applies a template to an item in GatherContent, replacing its fields. |
| [Create Item](actions/create-item.md) | POST | Creates a new item in GatherContent. |
| [Disconnect Template From Item](actions/disconnect-template-from-item.md) | PUT | Disconnects an item from its template in GatherContent. |
| [Duplicate Item](actions/duplicate-item.md) | POST | Duplicates an existing item in GatherContent. |
| [Get Item](actions/get-item.md) | GET | Retrieves an item from GatherContent. |
| [List Items](actions/list-items.md) | GET | Lists items in a GatherContent project. |
| [Move Item](actions/move-item.md) | PUT | Moves an existing item in GatherContent. |
| [Rename Item](actions/rename-item.md) | PUT | Renames an existing item in GatherContent. |
| [Update Item Content](actions/update-item-content.md) | PUT | Updates content for an existing item in GatherContent. |
| [Update Item Structure](actions/update-item-structure.md) | PUT | Updates the structure of an item in GatherContent. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [List Projects](actions/list-projects.md) | GET |  |

### Structure

| Action | Method | Description |
| --- | --- | --- |
| [Alter Structure](actions/alter-structure.md) | PUT | Updates a structure in GatherContent and applies changes to items. |
| [Get Structure](actions/get-structure.md) | GET | Retrieves a structure from GatherContent. |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Create Template](actions/create-template.md) | POST | Creates a new template in GatherContent. |
| [Delete Template](actions/delete-template.md) | DELETE | Deletes an existing template from GatherContent. |
| [Duplicate Template](actions/duplicate-template.md) | POST | Duplicates an existing template in GatherContent. |
| [Get Template](actions/get-template.md) | GET | Retrieves a template from GatherContent. |
| [List Templates](actions/list-templates.md) | GET | Lists templates in a GatherContent project. |
| [Rename Template](actions/rename-template.md) | PUT | Renames an existing template in GatherContent. |
| [Save Custom Structure As Template](actions/save-custom-structure-as-template.md) | POST | Creates a template from an item's custom structure in GatherContent. |
| [Save Structure As Template](actions/save-structure-as-template.md) | POST | Creates a template from a structure in GatherContent. |
| [Update Template Structure](actions/update-template-structure.md) | PUT | Updates the structure of a template in GatherContent. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET |  |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [List Webhooks](actions/list-webhooks.md) | GET | Lists subscribed webhooks in a GatherContent project. |
| [Subscribe To Webhook Event](actions/subscribe-to-webhook-event.md) | POST | Subscribes a webhook to an event in GatherContent. |

