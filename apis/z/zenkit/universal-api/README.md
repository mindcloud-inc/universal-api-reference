# <img src="https://images.mindcloud.co/apps/icons/zenkit_1773784371126.png" alt="Zenkit logo" width="28" height="28"> Zenkit: Universal API

Manage workspaces, lists, items, users, and comments

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zenkit/latest
- **Category:** Productivity / Project Management
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://zenkit.com/
- **Vendor API docs:** https://app.zenkit.com/docs/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zenkit/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Create List Entry Comment](actions/create-list-entry-comment.md) | POST | Creates a comment on a Zenkit item. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Add Element To List](actions/add-element-to-list.md) | POST | Creates a custom field in a Zenkit list. |
| [Get Elements In List](actions/get-elements-in-list.md) | GET | Retrieves custom fields from a Zenkit list. |
| [Update Element In List](actions/update-element-in-list.md) | PUT | Updates a custom field in a Zenkit list. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Create Entry](actions/create-entry.md) | POST | Creates a new item in Zenkit. |
| [Delete Deprecated Entry](actions/delete-deprecated-entry.md) | DELETE | Deletes a deprecated item from Zenkit. |
| [Filter Entries](actions/filter-entries.md) | GET | Retrieves filtered items from a Zenkit list. |
| [Get Entry](actions/get-entry.md) | GET | Retrieves an item from Zenkit. |
| [Get Filtered Entries For List View](actions/get-filtered-entries-for-list-view.md) | GET | Retrieves filtered items for a Zenkit list view. |
| [Search Entries](actions/search-entries.md) | GET | Searches for items in Zenkit. |
| [Update Entry](actions/update-entry.md) | PUT | Updates an existing item in Zenkit. |
| [Update Entry Field](actions/update-entry-field.md) | PUT | Updates a field on an existing Zenkit item. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Edit List Properties](actions/edit-list-properties.md) | PUT | Updates an existing list in Zenkit. |
| [Get List](actions/get-list.md) | GET | Retrieves a list from Zenkit. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Zenkit. |
| [Get Users For List](actions/get-users-for-list.md) | GET | Retrieves users for a Zenkit list. |
| [Get Users For Workspace](actions/get-users-for-workspace.md) | GET | Retrieves users for a Zenkit workspace. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Create Workspace](actions/create-workspace.md) | POST | Creates a new workspace in Zenkit. |
| [Deprecate Workspace](actions/deprecate-workspace.md) | DELETE | Deprecates an existing workspace in Zenkit. |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Zenkit. |
| [Get Workspaces And Lists](actions/get-workspaces-and-lists.md) | GET | Retrieves workspaces and lists from Zenkit. |
| [Update Workspace Details](actions/update-workspace-details.md) | PUT | Updates an existing workspace in Zenkit. |

