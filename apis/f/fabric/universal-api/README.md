# <img src="https://images.mindcloud.co/apps/icons/fabric_1775570557131.png" alt="Fabric logo" width="28" height="28"> Fabric: Universal API

Fabric API integration for workspaces, spaces, resources, memories, tags, uploads, search, and related content-management operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fabric/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 35
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://fabric.so
- **Vendor API docs:** https://developers.fabric.so/api-reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Workspace](actions/get-workspace.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-workspace?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (35)

### Bookmark

| Action | Method | Description |
| --- | --- | --- |
| [Create Bookmark](actions/create-bookmark.md) | POST | Creates a new bookmark in Fabric. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments for a resource from Fabric. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Create File](actions/create-file.md) | POST | Creates a new file in Fabric. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Create Folder](actions/create-folder.md) | POST | Creates a new folder in Fabric. |

### Memory

| Action | Method | Description |
| --- | --- | --- |
| [Create Memory](actions/create-memory.md) | POST | Creates a new memory in Fabric. |
| [Delete Memory](actions/delete-memory.md) | DELETE | Deletes a memory from Fabric. |
| [Get Memory](actions/get-memory.md) | GET | Retrieves a memory from Fabric. |
| [Search Memories](actions/search-memories.md) | GET | Finds memories in Fabric by semantic and keyword search. |
| [Update Memory](actions/update-memory.md) | PUT | Updates an existing memory in Fabric. |

### Memory Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Memory Job](actions/get-memory-job.md) | GET | Retrieves a memory job from Fabric. |

### Notepad

| Action | Method | Description |
| --- | --- | --- |
| [Create Notepad](actions/create-notepad.md) | POST | Creates a new notepad in Fabric. |

### Notepad Content

| Action | Method | Description |
| --- | --- | --- |
| [Get Notepad Content](actions/get-notepad-content.md) | GET | Retrieves notepad content from Fabric. |

### Resource

| Action | Method | Description |
| --- | --- | --- |
| [Delete Resources](actions/delete-resources.md) | DELETE | Deletes resources from Fabric. |
| [Get Resource](actions/get-resource.md) | GET | Retrieves a resource from Fabric. |
| [List Resources](actions/list-resources.md) | GET | Finds resources in Fabric by metadata filters. |
| [Recover Resources](actions/recover-resources.md) | PUT | Recovers deleted resources in Fabric. |
| [Update Resource](actions/update-resource.md) | PUT | Updates an existing resource in Fabric. |

### Resource Position

| Action | Method | Description |
| --- | --- | --- |
| [Reorder Resources](actions/reorder-resources.md) | PUT | Reorders resources in Fabric. |

### Resource Root

| Action | Method | Description |
| --- | --- | --- |
| [Get Resource Root](actions/get-resource-root.md) | GET | Retrieves a resource root from Fabric. |
| [List Resource Roots](actions/list-resource-roots.md) | GET | Retrieves resource roots from Fabric. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search](actions/search.md) | GET | Finds resources in Fabric by keyword or semantic search. |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [Create Space](actions/create-space.md) | POST | Creates a new space in Fabric. |
| [Delete Space](actions/delete-space.md) | DELETE | Deletes a space from Fabric. |
| [List Spaces](actions/list-spaces.md) | GET | Retrieves spaces from Fabric. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Get User Subscription](actions/get-user-subscription.md) | GET | Retrieves your subscription from Fabric. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in Fabric. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from Fabric. |

### Upload

| Action | Method | Description |
| --- | --- | --- |
| [Get Upload URL](actions/get-upload-url.md) | GET | Retrieves an upload URL from Fabric. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get My Profile](actions/get-my-profile.md) | GET | Retrieves your profile from Fabric. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST |  |
| [Delete Workspace](actions/delete-workspace.md) | DELETE |  |
| [Get Workspace](actions/get-workspace.md) | GET |  |
| [List Workspaces](actions/list-workspaces.md) | GET |  |
| [Update Workspace](actions/update-workspace.md) | PUT |  |

### Workspace Deletion Confirmation

| Action | Method | Description |
| --- | --- | --- |
| [Confirm Workspace Deletion](actions/confirm-workspace-deletion.md) | POST |  |

