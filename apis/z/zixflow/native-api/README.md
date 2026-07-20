# Zixflow: Native API Reference

A consolidated summary of Zixflow's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://docs.zixflow.com/api-reference/introduction
- **API base URL:** `https://api.zixflow.com/api/v1`

## Authentication

### API Key

Connect Zixflow with a bearer API key generated from Workspace Settings > Developer > API Key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.zixflow.com/api-reference/authentication)

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Activity](actions/create-activity.md) | `POST /collection-records/activity-list` | [docs](https://docs.zixflow.com/api-reference/activity-list/create) |
| [Create Collection Record](actions/create-collection-record.md) | `POST /collection-records/:collectionId` | [docs](https://docs.zixflow.com/api-reference/records/create) |
| [Create Custom Attribute](actions/create-custom-attribute.md) | `POST /attributes/:target/:targetId` | [docs](https://docs.zixflow.com/api-reference/attributes/create) |
| [Create List Entry](actions/create-list-entry.md) | `POST /list-entries/:listId` | [docs](https://docs.zixflow.com/api-reference/list-entries/create) |
| [Delete Collection Record By ID](actions/delete-collection-record-by-id.md) | `DELETE /collection-records/:collectionId/:recordId` | [docs](https://docs.zixflow.com/api-reference/records/delete) |
| [Delete List Entry By ID](actions/delete-list-entry-by-id.md) | `DELETE /list-entries/:listId/:entryId` | [docs](https://docs.zixflow.com/api-reference/list-entries/delete) |
| [Get Activity By ID](actions/get-activity-by-id.md) | `GET /collection-records/activity-list/:activityId` | [docs](https://docs.zixflow.com/api-reference/activity-list/get-by-id) |
| [Get Attribute By ID](actions/get-attribute-by-id.md) | `GET /attributes/:target/:targetId/:attributeId` | [docs](https://docs.zixflow.com/api-reference/attributes/get) |
| [Get Collection By ID](actions/get-collection-by-id.md) | `GET /collections/:collectionId` | [docs](https://docs.zixflow.com/api-reference/collection/get-collection) |
| [Get Collection Record By ID](actions/get-collection-record-by-id.md) | `GET /collection-records/:collectionId/:recordId` | [docs](https://docs.zixflow.com/api-reference/records/get-by-id) |
| [Get List By ID](actions/get-list-by-id.md) | `GET /lists/:listId` | [docs](https://docs.zixflow.com/api-reference/list/get-list) |
| [Get List Entry By ID](actions/get-list-entry-by-id.md) | `GET /list-entries/:listId/:entryId` | [docs](https://docs.zixflow.com/api-reference/list-entries/get-by-id) |
| [Get List of Activities](actions/get-list-of-activities.md) | `POST /collection-records/activity-list/query` | [docs](https://docs.zixflow.com/api-reference/activity-list/get) |
| [Get List of Attributes](actions/get-list-of-attributes.md) | `GET /attributes/:target/:targetId` | [docs](https://docs.zixflow.com/api-reference/attributes/get-list-of-attributes) |
| [Get List of Collection Records](actions/get-list-of-collection-records.md) | `POST /collection-records/:collectionId/query` | [docs](https://docs.zixflow.com/api-reference/records/get) |
| [Get List of Collections](actions/get-list-of-collections.md) | `GET /collections` | [docs](https://docs.zixflow.com/api-reference/collection/get-list-of-collections) |
| [Get List of List Entries](actions/get-list-of-list-entries.md) | `POST /list-entries/:listId/query` | [docs](https://docs.zixflow.com/api-reference/list-entries/get) |
| [Get List of Lists](actions/get-list-of-lists.md) | `GET /lists` | [docs](https://docs.zixflow.com/api-reference/list/get-list-of-lists) |
| [Get List of Workspace Members](actions/get-list-of-workspace-members.md) | `GET /workspace-members` | [docs](https://docs.zixflow.com/api-reference/workspace-members/get-list-of-members) |
| [Get WhatsApp Template Variables](actions/get-whatsapp-template-variables.md) | `GET /campaign/whatsapp/variable-keys` | [docs](https://docs.zixflow.com/api-reference/campaign/whatsapp/template-variable-get) |
| [Get Workspace Member By ID](actions/get-workspace-member-by-id.md) | `GET /workspace-members/:memberId` | [docs](https://docs.zixflow.com/api-reference/workspace-members/get) |
| [Update Activity](actions/update-activity.md) | `PATCH /collection-records/activity-list/:activityId` | [docs](https://docs.zixflow.com/api-reference/activity-list/edit) |
| [Update Collection Record](actions/update-collection-record.md) | `PATCH /collection-records/:collectionId/:recordId` | [docs](https://docs.zixflow.com/api-reference/records/edit) |
| [Update Custom Attribute](actions/update-custom-attribute.md) | `PATCH /attributes/:target/:targetId/:attributeId` | [docs](https://docs.zixflow.com/api-reference/attributes/update) |
| [Update List Entry](actions/update-list-entry.md) | `PATCH /list-entries/:listId/:entryId` | [docs](https://docs.zixflow.com/api-reference/list-entries/edit) |
