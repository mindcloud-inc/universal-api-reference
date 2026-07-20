# Asset Panda: Native API Reference

A consolidated summary of Asset Panda's API configuration and 50 documented operations, with links to official documentation.

- **Official docs:** https://team-asset-panda.readme.io/reference
- **API base URL:** `https://api.assetpanda.com`

## Authentication

### API Token

Use an Asset Panda access token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://team-asset-panda.readme.io/reference/generate-an-access-token)

## Endpoints (50 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Objects](actions/archive-objects.md) | `POST /v3/groups/:groupId/objects/archive` | [docs](https://team-asset-panda.readme.io/reference/post_v3-groups-group-id-objects-archive) |
| [Attach Attachment to Object](actions/attach-attachment-to-object.md) | `PUT /v3/groups/:groupId/objects/:groupObjectId/attachment/:attachmentId/attach` | [docs](https://team-asset-panda.readme.io/reference/put_v3-groups-group-id-objects-group-object-id-attachment-attachment-id-attach) |
| [Create Account User](actions/create-account-user.md) | `POST /v3/accounts` | [docs](https://team-asset-panda.readme.io/reference/post_v3-accounts) |
| [Create Folder](actions/create-folder.md) | `POST /v3/attachment/folders/:folderId` | [docs](https://team-asset-panda.readme.io/reference/post_v3-attachment-folders-folder-id) |
| [Create Group Action](actions/create-group-action.md) | `POST /v3/groups/:groupId/actions` | [docs](https://team-asset-panda.readme.io/reference/post_v3-groups-group-id-actions) |
| [Create Multiple](actions/create-multiple.md) | `POST /v3/entity_objects/action_objects/:id/create_multiple` | [docs](https://team-asset-panda.readme.io/reference/post_v3-entity-objects-action-objects-id-create-multiple) |
| [Create Multiple Action Fields](actions/create-multiple-action-fields.md) | `POST /v3/actions/:actionId/fields` | [docs](https://team-asset-panda.readme.io/reference/post_v3-actions-action-id-fields) |
| [Create Object](actions/create-object.md) | `POST /v3/groups/:groupId/objects` | [docs](https://team-asset-panda.readme.io/reference/post_v3-groups-group-id-objects) |
| [Create Report](actions/create-report.md) | `POST /v3/reports` | [docs](https://team-asset-panda.readme.io/reference/post_v3-reports) |
| [Create User](actions/create-user.md) | `POST /v3/users` | [docs](https://team-asset-panda.readme.io/reference/post_v3-users) |
| [Delete Account](actions/delete-account.md) | `DELETE /v3/accounts/:accountId` | [docs](https://team-asset-panda.readme.io/reference/delete_v3-accounts-account-id) |
| [Delete Action Field](actions/delete-action-field.md) | `DELETE /v3/actions/:actionId/fields/:fieldId` | [docs](https://team-asset-panda.readme.io/reference/delete_v3-actions-action-id-fields-field-id) |
| [Delete Attachment](actions/delete-attachment.md) | `DELETE /v3/attachments` | [docs](https://team-asset-panda.readme.io/reference/delete_v3-attachments) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /v3/attachment/folders/:folderId` | [docs](https://team-asset-panda.readme.io/reference/delete_v3-attachment-folders-folder-id) |
| [Delete Report](actions/delete-report.md) | `DELETE /v3/reports/:reportId` | [docs](https://team-asset-panda.readme.io/reference/delete_v3-reports-report-id) |
| [Detach Attachment from Object](actions/detach-attachment-from-object.md) | `PUT /v3/groups/:groupId/objects/:groupObjectId/attachment/:attachmentId/detach` | [docs](https://team-asset-panda.readme.io/reference/put_v3-groups-group-id-objects-group-object-id-attachment-attachment-id-detach) |
| [Generate Report](actions/generate-report.md) | `GET /v3/reports/:reportId` | [docs](https://team-asset-panda.readme.io/reference/get_v3-reports-report-id) |
| [Get Account Details](actions/get-account-details.md) | `GET /v3/accounts/:accountId` | [docs](https://team-asset-panda.readme.io/reference/get_v3-accounts-account-id) |
| [Get Action](actions/get-action.md) | `GET /v3/actions/:actionId` | [docs](https://team-asset-panda.readme.io/reference/get_v3-actions-action-id) |
| [Get Action Group](actions/get-action-group.md) | `GET /v3/actions/:actionId/group` | [docs](https://team-asset-panda.readme.io/reference/get_v3-actions-action-id-group) |
| [Get Group](actions/get-group.md) | `GET /v3/groups/:groupId` | [docs](https://team-asset-panda.readme.io/reference/get_v3-groups-group-id) |
| [Link Attachment to Object](actions/link-attachment-to-object.md) | `POST /v3/group/objects/:groupObjectId/attachments` | [docs](https://team-asset-panda.readme.io/reference/post_v3-group-objects-group-object-id-attachments) |
| [List Action Fields](actions/list-action-fields.md) | `GET /v3/actions/:actionId/fields` | [docs](https://team-asset-panda.readme.io/reference/get_v3-actions-action-id-fields) |
| [List Action Objects](actions/list-action-objects.md) | `GET /v3/entity_objects/:objectId/action_objects` | [docs](https://team-asset-panda.readme.io/reference/get_v3-entity-objects-object-id-action-objects) |
| [List Actions](actions/list-actions.md) | `GET /v3/actions` | [docs](https://team-asset-panda.readme.io/reference/get_v3-actions) |
| [List Attachments](actions/list-attachments.md) | `GET /v3/attachments` | [docs](https://team-asset-panda.readme.io/reference/get_v3-attachments) |
| [List Change Logs](actions/list-change-logs.md) | `GET /v3/entity_objects/:objectId/change_logs` | [docs](https://team-asset-panda.readme.io/reference/get_v3-entity-objects-object-id-change-logs) |
| [List Group Action Fields](actions/list-group-action-fields.md) | `GET /v3/groups/:groupId/actions/:actionId/fields` | [docs](https://team-asset-panda.readme.io/reference/get_v3-groups-group-id-actions-action-id-fields) |
| [List Group Actions](actions/list-group-actions.md) | `GET /v3/groups/:groupId/actions` | [docs](https://team-asset-panda.readme.io/reference/get_v3-groups-group-id-actions) |
| [List Group Fields](actions/list-group-fields.md) | `GET /v3/groups/:groupId/fields` | [docs](https://team-asset-panda.readme.io/reference/get_v3-groups-group-id-fields) |
| [List Group Statuses](actions/list-group-statuses.md) | `GET /v3/groups/:groupId/statuses` | [docs](https://team-asset-panda.readme.io/reference/get_v3-groups-group-id-statuses) |
| [List Groups](actions/list-groups.md) | `GET /v3/groups` | [docs](https://team-asset-panda.readme.io/reference/get_v3-groups) |
| [List Linked Fields](actions/list-linked-fields.md) | `GET /v3/entity_objects/:id/linked_fields` | [docs](https://team-asset-panda.readme.io/reference/get_v3-entity-objects-id-linked-fields) |
| [List Linked Objects](actions/list-linked-objects.md) | `GET /v3/entity_objects/:id/linked_objects/:fieldId` | [docs](https://team-asset-panda.readme.io/reference/get_v3-entity-objects-id-linked-objects-field-id) |
| [List Reports](actions/list-reports.md) | `GET /v3/reports` | [docs](https://team-asset-panda.readme.io/reference/get_v3-reports) |
| [List Returnable Action Objects](actions/list-returnable-action-objects.md) | `GET /v3/entity_objects/:objectId/action_objects/:actionId/returnable_action_objects` | [docs](https://team-asset-panda.readme.io/reference/get_v3-entity-objects-object-id-action-objects-action-id-returnable-action-objects) |
| [List User Templates](actions/list-user-templates.md) | `GET /v3/users/templates` | [docs](https://team-asset-panda.readme.io/reference/get_v3-users-templates) |
| [List Users](actions/list-users.md) | `GET /v3/users` | [docs](https://team-asset-panda.readme.io/reference/get_v3-users) |
| [Retrieve Self Details](actions/retrieve-self-details.md) | `GET /v3/users/me` | [docs](https://team-asset-panda.readme.io/reference/get_v3-users-me) |
| [Retrieve Settings](actions/retrieve-settings.md) | `GET /v3/settings` | [docs](https://team-asset-panda.readme.io/reference/get_v3-settings) |
| [Return Multiple](actions/return-multiple.md) | `POST /v3/entity_objects/action_objects/:id/return_multiple` | [docs](https://team-asset-panda.readme.io/reference/post_v3-entity-objects-action-objects-id-return-multiple) |
| [Return Object](actions/return-object.md) | `POST /v3/entity_objects/action_objects/:actionId/return_object` | [docs](https://team-asset-panda.readme.io/reference/post_v3-entity-objects-action-objects-action-id-return-object) |
| [Search Objects](actions/search-objects.md) | `POST /v3/groups/:groupId/search/objects` | [docs](https://team-asset-panda.readme.io/reference/post_v3-groups-group-id-search-objects) |
| [Unarchive Objects](actions/unarchive-objects.md) | `POST /v3/groups/:groupId/objects/unarchive` | [docs](https://team-asset-panda.readme.io/reference/post_v3-groups-group-id-objects-unarchive) |
| [Update Action Field](actions/update-action-field.md) | `PUT /v3/actions/:actionId/fields/:fieldId` | [docs](https://team-asset-panda.readme.io/reference/put_v3-actions-action-id-fields-field-id) |
| [Update Attachment](actions/update-attachment.md) | `PUT /v3/attachments/:attachmentId` | [docs](https://team-asset-panda.readme.io/reference/put_v3-attachments-attachment-id) |
| [Update Group Object](actions/update-group-object.md) | `PATCH /v3/groups/:groupId/objects/:objectId` | [docs](https://team-asset-panda.readme.io/reference/patch_v3-groups-group-id-objects-object-id) |
| [Update Multiple Objects](actions/update-multiple-objects.md) | `PUT /v3/groups/:groupId/objects` | [docs](https://team-asset-panda.readme.io/reference/put_v3-groups-group-id-objects) |
| [Update Report](actions/update-report.md) | `PUT /v3/reports/:reportId` | [docs](https://team-asset-panda.readme.io/reference/put_v3-reports-report-id) |
| [Update User](actions/update-user.md) | `PUT /v3/users/:userId` | [docs](https://team-asset-panda.readme.io/reference/put_v3-users-user-id) |
