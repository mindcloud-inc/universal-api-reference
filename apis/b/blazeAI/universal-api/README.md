# <img src="https://images.mindcloud.co/apps/icons/blaze-ai_1775235135127.png" alt="Blaze AI logo" width="28" height="28"> Blaze AI: Universal API

Connect to Blaze AI workspaces and manage docs, folders, handbooks, properties, subscriptions, imports, groups, users, and brand voices through the official Blaze API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/blazeAI/latest
- **Category:** Artificial Intelligence / AI / ML
- **Actions:** 33
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.blaze.ai
- **Vendor API docs:** https://api.blaze.ai/api/documentation

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Workspaces](actions/list-workspaces.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blazeAI/latest/actions/list-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (33)

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Add Doc Property](actions/add-doc-property.md) | POST | Creates a document property in Blaze AI. |
| [Create Workspace Property](actions/create-workspace-property.md) | POST | Creates a workspace property in Blaze AI. |
| [Delete Workspace Property](actions/delete-workspace-property.md) | DELETE | Deletes an existing workspace property from Blaze AI. |
| [List Doc Properties](actions/list-doc-properties.md) | GET | Retrieves document properties from Blaze AI. |
| [List Workspace Properties](actions/list-workspace-properties.md) | GET | Retrieves workspace properties from Blaze AI. |
| [Remove Doc Property](actions/remove-doc-property.md) | DELETE | Deletes an existing document property from Blaze AI. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Generate Doc](actions/generate-doc.md) | POST | Creates an AI-generated document in Blaze AI. |
| [Get Doc](actions/get-doc.md) | GET | Retrieves a document from Blaze AI. |
| [List Docs](actions/list-docs.md) | GET | Retrieves documents from a Blaze AI workspace. |
| [Update Doc](actions/update-doc.md) | PUT | Updates an existing document in Blaze AI. |

### Files

| Action | Method | Description |
| --- | --- | --- |
| [Move Files](actions/move-files.md) | PUT | Moves files between folders in Blaze AI. |

### Folders

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Blaze AI. |
| [Get Folder](actions/get-folder.md) | GET | Retrieves a folder from Blaze AI. |
| [List Folders](actions/list-folders.md) | GET | Retrieves folders from a Blaze AI workspace. |
| [Update Folder](actions/update-folder.md) | PUT | Updates an existing folder in Blaze AI. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Groups](actions/list-groups.md) | GET | Retrieves workspace groups from Blaze AI. |

### Import Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Get Import](actions/get-import.md) | GET | Retrieves a document import from Blaze AI. |
| [Import Doc](actions/import-doc.md) | POST | Creates a document import in Blaze AI. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Add Handbook Item](actions/add-handbook-item.md) | POST | Creates a handbook item in Blaze AI. |
| [Delete Handbook Item](actions/delete-handbook-item.md) | DELETE | Deletes an existing handbook item from Blaze AI. |
| [List Handbook Items](actions/list-handbook-items.md) | GET | Retrieves handbook items from Blaze AI. |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [Add Doc Access](actions/add-doc-access.md) | POST | Creates a document access in Blaze AI. |
| [List Doc Accesses](actions/list-doc-accesses.md) | GET | Retrieves document accesses from Blaze AI. |
| [Remove Doc Access](actions/remove-doc-access.md) | DELETE | Deletes an existing document access from Blaze AI. |
| [Update Doc Access](actions/update-doc-access.md) | PUT | Updates an existing document access in Blaze AI. |

### Subscriptions

| Action | Method | Description |
| --- | --- | --- |
| [Create Published Doc Subscription](actions/create-published-doc-subscription.md) | POST | Creates a published document subscription in Blaze AI. |
| [Delete Published Doc Subscription](actions/delete-published-doc-subscription.md) | DELETE | Deletes an existing published document subscription from Blaze AI. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get Published Docs Polling Test](actions/get-published-docs-polling-test.md) | GET | Retrieves published document polling test data from Blaze AI. |
| [List Brand Voices](actions/list-brand-voices.md) | GET | Retrieves brand voices from Blaze AI. |
| [List Handbooks](actions/list-handbooks.md) | GET | Retrieves available handbooks from Blaze AI. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Group Users](actions/list-group-users.md) | GET | Retrieves users from a Blaze AI group. |
| [List Users](actions/list-users.md) | GET | Retrieves users from a Blaze AI workspace. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces](actions/list-workspaces.md) | GET | Retrieves available workspaces from Blaze AI. |

