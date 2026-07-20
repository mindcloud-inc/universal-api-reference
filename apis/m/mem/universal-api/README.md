# <img src="https://images.mindcloud.co/apps/icons/memdotai-logo_1773431978782.jpeg" alt="Mem logo" width="28" height="28"> Mem: Universal API

Capture notes, search ideas, and manage collections in Mem

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/mem/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://get.mem.ai
- **Vendor API docs:** https://docs.mem.ai/api-reference/overview/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Notes](actions/list-notes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mem/latest/actions/list-notes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | POST | Creates a new collection in Mem. |
| [Delete Collection](actions/delete-collection.md) | DELETE | Deletes an existing collection from Mem. |
| [Get Collection](actions/get-collection.md) | GET | Retrieves a collection from Mem. |
| [List Collections](actions/list-collections.md) | GET | Retrieves collections from Mem. |
| [Search Collections](actions/search-collections.md) | GET | Finds collections in Mem by search query. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Note](actions/create-note.md) | POST | Creates a new note in Mem. |
| [Delete Note](actions/delete-note.md) | DELETE | Deletes an existing note from Mem. |
| [Get Note](actions/get-note.md) | GET | Retrieves a note from Mem. |
| [List Notes](actions/list-notes.md) | GET | Retrieves notes from Mem. |
| [Search Notes](actions/search-notes.md) | GET | Finds notes in Mem by search query. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Mem It](actions/mem-it.md) | POST | Creates a note in Mem from raw input. |

