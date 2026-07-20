# <img src="https://images.mindcloud.co/apps/icons/histre_1776452393207.png" alt="Histre logo" width="28" height="28"> Histre: Universal API

Organize research, notes, highlights, collections, and shared team knowledge in Histre.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/histre/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 21
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://histre.com/
- **Vendor API docs:** https://histre.com/features/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve User Settings](actions/retrieve-user-settings.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/histre/latest/actions/retrieve-user-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (21)

### Auth Tokens

| Action | Method | Description |
| --- | --- | --- |
| [Obtain Auth Tokens](actions/obtain-auth-tokens.md) | GET | Obtains authentication tokens from Histre for API access. |

### Collection

| Action | Method | Description |
| --- | --- | --- |
| [Create a New Collection](actions/create-new-collection.md) | POST | Creates a new collection in Histre. |
| [Retrieve Collection Details](actions/retrieve-collection-details.md) | GET | Retrieves collection details from Histre. |
| [Update Collection Details](actions/update-collection-details.md) | PUT | Updates collection details in Histre. |

### Collection Delete Result

| Action | Method | Description |
| --- | --- | --- |
| [Delete a Collection](actions/delete-collection.md) | DELETE | Deletes a collection from Histre. |

### Collection Note Add Result

| Action | Method | Description |
| --- | --- | --- |
| [Add Notes to Collections](actions/add-notes-to-collections.md) | PUT | Adds notes to collections in Histre. |

### Collection Note Remove Result

| Action | Method | Description |
| --- | --- | --- |
| [Remove Note from Collections](actions/remove-note-from-collections.md) | PUT | Removes a note from collections in Histre. |

### Collection Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Search for Collections](actions/search-collections.md) | GET | Finds collections in Histre by search query. |

### Collections

| Action | Method | Description |
| --- | --- | --- |
| [List All Collections](actions/list-all-collections.md) | GET | Retrieves collections from Histre. |

### Highlight Delete Result

| Action | Method | Description |
| --- | --- | --- |
| [Delete Highlight](actions/delete-highlight.md) | DELETE | Deletes a highlight from Histre. |

### Highlight Save Result

| Action | Method | Description |
| --- | --- | --- |
| [Save Page Highlights](actions/save-page-highlights.md) | POST | Creates page highlights in Histre. |

### Highlight Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Search for Highlights](actions/search-highlights.md) | GET | Finds highlights in Histre by search query. |

### Highlight Update Result

| Action | Method | Description |
| --- | --- | --- |
| [Update a Highlight](actions/update-highlight.md) | PUT | Updates a highlight in Histre. |

### Highlights

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Page Highlights](actions/retrieve-page-highlights.md) | GET | Retrieves page highlights from Histre. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve a Note](actions/retrieve-note.md) | GET | Retrieves a note from Histre. |

### Note Delete Result

| Action | Method | Description |
| --- | --- | --- |
| [Delete a Note](actions/delete-note.md) | DELETE | Deletes a note from Histre. |

### Note Mutation Result

| Action | Method | Description |
| --- | --- | --- |
| [Create Or Update Notes](actions/create-or-update-notes.md) | POST | Creates or updates notes in Histre. |

### Note Search Results

| Action | Method | Description |
| --- | --- | --- |
| [Search Notes](actions/search-notes.md) | GET | Finds notes in Histre by search query. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [List Notes](actions/list-notes.md) | GET | Retrieves notes from Histre. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Tags](actions/retrieve-tags.md) | GET | Retrieves tags from Histre. |

### User Settings

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve User Settings](actions/retrieve-user-settings.md) | GET | Retrieves user settings from Histre. |

