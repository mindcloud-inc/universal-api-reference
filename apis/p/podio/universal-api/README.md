# <img src="https://images.mindcloud.co/apps/icons/podio_1773167825091.png" alt="Podio logo" width="28" height="28"> Podio: Universal API

Manage workspaces, items, tasks, and collaboration in Podio

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/podio/latest
- **Category:** Productivity / Project Management
- **Actions:** 25
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://podio.com
- **Vendor API docs:** https://developers.podio.com/doc

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Status](actions/get-user-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podio/latest/actions/get-user-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (25)

### App

| Action | Method | Description |
| --- | --- | --- |
| [Get App](actions/get-app.md) | GET | Retrieves an existing app from Podio. |
| [List Apps](actions/list-apps.md) | GET | Retrieves a list of apps from Podio. |
| [List Apps by Space](actions/list-apps-by-space.md) | GET | Retrieves apps in a Podio space. |

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Attach File](actions/attach-file.md) | POST | Attaches a file to a Podio object. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add Comment to Object](actions/add-comment-to-object.md) | POST | Creates a comment on a Podio object. |
| [List Comments on Object](actions/list-comments-on-object.md) | GET | Retrieves comments on a Podio object. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Uploads a file to Podio. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Add Item](actions/add-item.md) | POST | Creates a new item in Podio. |
| [Delete Item](actions/delete-item.md) | DELETE | Deletes an existing item from Podio. |
| [Filter Items](actions/filter-items.md) | GET | Finds items in Podio using filters. |
| [Filter Items by View](actions/filter-items-by-view.md) | GET | Finds items in a Podio view. |
| [Get Item](actions/get-item.md) | GET | Retrieves an existing item from Podio. |
| [Update Item](actions/update-item.md) | PUT | Updates an existing item in Podio. |

### Item Values

| Action | Method | Description |
| --- | --- | --- |
| [Get Item Values v2](actions/get-item-values-v2.md) | GET | Retrieves item values from Podio. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search in Application v2](actions/search-in-application-v2.md) | GET | Finds results in a Podio application. |
| [Search in Space v2](actions/search-in-space-v2.md) | GET | Finds results in a Podio space. |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [Get Space](actions/get-space.md) | GET | Retrieves an existing space from Podio. |
| [List Top Spaces](actions/list-top-spaces.md) | GET | Retrieves top spaces from Podio. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Complete Task](actions/complete-task.md) | PUT | Marks an existing task complete in Podio. |
| [Create Task](actions/create-task.md) | POST | Creates a new task in Podio. |
| [Get Task](actions/get-task.md) | GET | Retrieves an existing task from Podio. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves a list of tasks from Podio. |
| [Update Task](actions/update-task.md) | PUT | Updates an existing task in Podio. |

### User Status

| Action | Method | Description |
| --- | --- | --- |
| [Get User Status](actions/get-user-status.md) | GET | Retrieves user status details from Podio. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Workspaces](actions/list-organization-workspaces.md) | GET | Retrieves organization workspaces from Podio. |

