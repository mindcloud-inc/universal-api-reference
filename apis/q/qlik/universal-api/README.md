# <img src="https://images.mindcloud.co/apps/icons/qlik_1776715282461.png" alt="Qlik logo" width="28" height="28"> Qlik: Universal API

Connect to Qlik Cloud tenant REST APIs to manage apps, spaces, users, groups, items, collections, reloads, and operational content.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/qlik/latest
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.qlik.com
- **Vendor API docs:** https://qlik.dev/apis/rest/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qlik/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### App

| Action | Method | Description |
| --- | --- | --- |
| [Copy App](actions/copy-app.md) | POST | Creates a copy of an app in Qlik. |
| [Create App](actions/create-app.md) | POST | Creates a new app in Qlik. |
| [Get App](actions/get-app.md) | GET | Retrieves an app from your Qlik tenant. |
| [Update App](actions/update-app.md) | PUT | Updates an existing app in Qlik. |

### App Export

| Action | Method | Description |
| --- | --- | --- |
| [Export App](actions/export-app.md) | GET | Exports an existing app from Qlik. |

### App Lineage

| Action | Method | Description |
| --- | --- | --- |
| [Get App Lineage](actions/get-app-lineage.md) | GET | Retrieves lineage data for an app in Qlik. |

### App Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get App Metadata](actions/get-app-metadata.md) | GET | Retrieves metadata for an app in Qlik. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in Qlik. |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a collection from your Qlik tenant. |
| [Get Favorites Collection](actions/get-favorites-collection.md) | GET | Retrieves the favorites collection from Qlik. |
| [List Collections](actions/list-collections.md) | GET | Retrieves collections from your Qlik tenant. |
| [List Item Collections](actions/list-item-collections.md) | GET | Retrieves the collections for an item in Qlik. |
| [Update Collection](actions/update-collection.md) | PUT | Updates an existing collection in Qlik. |

### Collection Item

| Action | Method | Description |
| --- | --- | --- |
| [Add Item To Collection](actions/add-item-to-collection.md) | POST | Adds an item to a collection in Qlik. |
| [List Collection Items](actions/list-collection-items.md) | GET | Retrieves items from a collection in Qlik. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Filter Groups](actions/filter-groups.md) | GET | Finds groups in Qlik by advanced filter query. |
| [Get Group](actions/get-group.md) | GET | Retrieves a group from your Qlik tenant. |
| [List Groups](actions/list-groups.md) | GET | Retrieves groups from your Qlik tenant. |

### Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Item](actions/get-item.md) | GET | Retrieves an item from your Qlik tenant. |
| [List Items](actions/list-items.md) | GET | Retrieves items from your Qlik tenant. |
| [Update Item](actions/update-item.md) | PUT | Updates an existing item in Qlik. |

### Published Item

| Action | Method | Description |
| --- | --- | --- |
| [List Published Items](actions/list-published-items.md) | GET | Retrieves published copies of an item in Qlik. |

### Reload

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Reload](actions/cancel-reload.md) | PUT | Cancels an existing reload in Qlik. |
| [Get Reload](actions/get-reload.md) | GET | Retrieves a reload from your Qlik tenant. |
| [List Reloads](actions/list-reloads.md) | GET | Retrieves reloads from your Qlik tenant. |
| [Trigger App Reload](actions/trigger-app-reload.md) | POST | Triggers an app reload in Qlik. |

### Reload Task

| Action | Method | Description |
| --- | --- | --- |
| [List Reload Tasks](actions/list-reload-tasks.md) | GET | Retrieves reload tasks from your Qlik tenant. |

### Space

| Action | Method | Description |
| --- | --- | --- |
| [Create Space](actions/create-space.md) | POST | Creates a new space in your Qlik tenant. |
| [Get Space](actions/get-space.md) | GET | Retrieves a space from your Qlik tenant. |
| [List Spaces](actions/list-spaces.md) | GET | Retrieves spaces from your Qlik tenant. |
| [Update Space Properties](actions/update-space-properties.md) | PUT | Updates an existing space's properties in Qlik. |

### Space Assignment

| Action | Method | Description |
| --- | --- | --- |
| [Assign Space Member](actions/assign-space-member.md) | POST | Assigns a user or group to a space in Qlik. |
| [List Space Assignments](actions/list-space-assignments.md) | GET | Retrieves assignments for a space in Qlik. |
| [Update Space Assignment](actions/update-space-assignment.md) | PUT | Updates an existing space assignment in Qlik. |

### Space Type

| Action | Method | Description |
| --- | --- | --- |
| [List Space Types](actions/list-space-types.md) | GET | Retrieves available space types from your Qlik tenant. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Count Users](actions/count-users.md) | GET | Retrieves the user count for your Qlik tenant. |
| [Filter Users](actions/filter-users.md) | GET | Finds users in Qlik by advanced filter query. |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from Qlik. |
| [Get User](actions/get-user.md) | GET | Retrieves a user from your Qlik tenant. |
| [List Users](actions/list-users.md) | GET | Retrieves users from your Qlik tenant. |

