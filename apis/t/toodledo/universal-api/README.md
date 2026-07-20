# <img src="https://images.mindcloud.co/apps/icons/toodledo_1773677018875.png" alt="Toodledo logo" width="28" height="28"> Toodledo: Universal API

Toodledo: Manage tasks, notes, outlines, and custom lists

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/toodledo/latest
- **Category:** Productivity / Project Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.toodledo.com/
- **Vendor API docs:** https://api.toodledo.com/3/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account Info](actions/get-account-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Collaborator

| Action | Method | Description |
| --- | --- | --- |
| [List Collaborators](actions/list-collaborators.md) | GET | Retrieves collaborators from Toodledo. |

### List

| Action | Method | Description |
| --- | --- | --- |
| [Create Lists](actions/create-lists.md) | POST | Creates lists in Toodledo. |
| [Delete Lists](actions/delete-lists.md) | DELETE | Deletes existing lists from Toodledo. |
| [List Deleted Lists](actions/list-deleted-lists.md) | GET | Retrieves deleted lists from Toodledo. |
| [List Lists](actions/list-lists.md) | GET | Retrieves lists from Toodledo. |
| [Update Lists](actions/update-lists.md) | PUT | Updates existing lists in Toodledo. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Notes](actions/create-notes.md) | POST | Creates notes in Toodledo. |
| [Delete Notes](actions/delete-notes.md) | DELETE | Deletes existing notes from Toodledo. |
| [List Deleted Notes](actions/list-deleted-notes.md) | GET | Retrieves deleted notes from Toodledo. |
| [List Notes](actions/list-notes.md) | GET | Retrieves notes from Toodledo. |
| [Update Notes](actions/update-notes.md) | PUT | Updates existing notes in Toodledo. |

### Outline

| Action | Method | Description |
| --- | --- | --- |
| [Create Outlines](actions/create-outlines.md) | POST | Creates outlines in Toodledo. |
| [Delete Outlines](actions/delete-outlines.md) | DELETE | Deletes existing outlines from Toodledo. |
| [List Deleted Outlines](actions/list-deleted-outlines.md) | GET | Retrieves deleted outlines from Toodledo. |
| [List Outlines](actions/list-outlines.md) | GET | Retrieves outlines from Toodledo. |
| [Update Outlines](actions/update-outlines.md) | PUT | Updates existing outlines in Toodledo. |

### Row

| Action | Method | Description |
| --- | --- | --- |
| [Create Rows](actions/create-rows.md) | POST | Creates rows in Toodledo. |
| [Delete Rows](actions/delete-rows.md) | DELETE | Deletes existing rows from Toodledo. |
| [List Deleted Rows](actions/list-deleted-rows.md) | GET | Retrieves deleted rows from Toodledo. |
| [List Rows](actions/list-rows.md) | GET | Retrieves rows from Toodledo. |
| [Update Rows](actions/update-rows.md) | PUT | Updates existing rows in Toodledo. |

### Saved Search

| Action | Method | Description |
| --- | --- | --- |
| [List Saved Searches](actions/list-saved-searches.md) | GET | Retrieves saved searches from Toodledo. |

### Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Tasks](actions/create-tasks.md) | POST | Creates tasks in Toodledo. |
| [Delete Tasks](actions/delete-tasks.md) | DELETE | Deletes existing tasks from Toodledo. |
| [List Deleted Tasks](actions/list-deleted-tasks.md) | GET | Retrieves deleted tasks from Toodledo. |
| [List Tasks](actions/list-tasks.md) | GET | Retrieves tasks from Toodledo. |
| [Reassign Task](actions/reassign-task.md) | PUT | Reassigns a task to a collaborator in Toodledo. |
| [Share Task](actions/share-task.md) | PUT | Shares a task with a collaborator in Toodledo. |
| [Update Tasks](actions/update-tasks.md) | PUT | Updates existing tasks in Toodledo. |

### User Profile

| Action | Method | Description |
| --- | --- | --- |
| [Get Account Info](actions/get-account-info.md) | GET | Retrieves account details from Toodledo. |

