# <img src="https://images.mindcloud.co/apps/icons/link-ace_1775251445931.png" alt="LinkAce logo" width="28" height="28"> LinkAce: Universal API

LinkAce is an open-source bookmark archive and manager for links, lists, tags, notes, trash, and bulk curation workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/linkAce/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.linkace.org
- **Vendor API docs:** https://api-docs.linkace.org/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Links](actions/list-links.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkAce/latest/actions/list-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Labels

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a new tag in LinkAce. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes an existing tag from LinkAce. |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a specific tag from LinkAce. |
| [List Tags](actions/list-tags.md) | GET | Retrieves saved bookmark tags from LinkAce. |
| [Search Tags](actions/search-tags.md) | GET | Finds tags in LinkAce for link editing. |
| [Update Tag](actions/update-tag.md) | PUT | Updates an existing tag in LinkAce. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in LinkAce. |
| [Delete List](actions/delete-list.md) | DELETE | Deletes an existing list from LinkAce. |
| [Get List](actions/get-list.md) | GET | Retrieves a specific list from LinkAce. |
| [List Lists](actions/list-lists.md) | GET | Retrieves saved bookmark lists from LinkAce. |
| [Search Lists](actions/search-lists.md) | GET | Finds lists in LinkAce for link editing. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in LinkAce. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a new note in LinkAce. |
| [Delete Note](actions/delete-note.md) | DELETE | Deletes an existing note from LinkAce. |
| [List Notes for Link](actions/list-notes-for-link.md) | GET | Retrieves notes for a specific link in LinkAce. |
| [Update Note](actions/update-note.md) | PUT | Updates an existing note in LinkAce. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Delete Links](actions/bulk-delete-links.md) | DELETE |  |
| [Bulk Edit Links](actions/bulk-edit-links.md) | PUT | Updates multiple bookmark links in LinkAce. |
| [Bulk Store Links](actions/bulk-store-links.md) | POST | Creates multiple bookmark links in LinkAce. |
| [Clear Trash](actions/clear-trash.md) | DELETE | Deletes trashed entries from LinkAce for a specific model. |
| [Create Link](actions/create-link.md) | POST | Creates a new link in LinkAce. |
| [Delete Link](actions/delete-link.md) | DELETE | Deletes an existing link from LinkAce. |
| [Get Link](actions/get-link.md) | GET | Retrieves a specific link from LinkAce. |
| [List Links](actions/list-links.md) | GET | Retrieves saved bookmark links from LinkAce. |
| [List Links for List](actions/list-links-for-list.md) | GET | Retrieves links from a specific list in LinkAce. |
| [List Links for Tag](actions/list-links-for-tag.md) | GET | Retrieves links for a specific tag in LinkAce. |
| [List Trash Links](actions/list-trash-links.md) | GET | Retrieves trashed bookmark links from LinkAce. |
| [Restore Trash Entry](actions/restore-trash-entry.md) | PUT | Restores a trashed entry in LinkAce. |
| [Search Links](actions/search-links.md) | GET | Finds matching bookmark links in LinkAce. |
| [Update Link](actions/update-link.md) | PUT | Updates an existing link in LinkAce. |

