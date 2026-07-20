# <img src="https://images.mindcloud.co/apps/icons/readwise_1773849623765.png" alt="Readwise logo" width="28" height="28"> Readwise: Universal API

Readwise lets users save, review, sync, and export reading highlights and Reader documents.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/readwise/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 43
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://readwise.io
- **Vendor API docs:** https://readwise.io/reader_api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Validate Connection](actions/validate-connection.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/readwise/latest/actions/validate-connection?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (43)

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Validate Connection](actions/validate-connection.md) | GET | Validates the connected Readwise access token. |

### Book

| Action | Method | Description |
| --- | --- | --- |
| [Export Highlights](actions/export-highlights.md) | GET | Retrieves books and highlights from Readwise. |
| [Get Book](actions/get-book.md) | GET | Retrieves a book from the Readwise library. |
| [List Books](actions/list-books.md) | GET | Retrieves books from the Readwise library. |

### Book Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Book Tag](actions/add-book-tag.md) | POST | Creates a new tag for a Readwise book. |
| [Get Book Tag](actions/get-book-tag.md) | GET | Retrieves a tag from a Readwise book. |
| [Remove Book Tag](actions/remove-book-tag.md) | DELETE | Deletes a tag from a Readwise book. |
| [Update Book Tag](actions/update-book-tag.md) | PUT | Updates an existing tag on a Readwise book. |

### Highlight

| Action | Method | Description |
| --- | --- | --- |
| [Add Tags To Reader Highlight](actions/add-tags-to-reader-highlight.md) | PUT | Adds tags to a highlight in Readwise Reader. |
| [Create Highlights](actions/create-highlights.md) | POST | Creates new highlights in the Readwise library. |
| [Create Reader Highlight](actions/create-reader-highlight.md) | POST | Creates a new highlight in Readwise Reader. |
| [Delete Highlight](actions/delete-highlight.md) | DELETE | Deletes an existing highlight from Readwise. |
| [Get Highlight](actions/get-highlight.md) | GET | Retrieves a highlight from the Readwise library. |
| [Get Reader Document Highlights](actions/get-reader-document-highlights.md) | GET | Retrieves highlights for a Readwise Reader document. |
| [List Highlights](actions/list-highlights.md) | GET | Retrieves highlights from the Readwise library. |
| [Remove Tags From Reader Highlight](actions/remove-tags-from-reader-highlight.md) | PUT | Removes tags from a highlight in Readwise Reader. |
| [Search Readwise Highlights](actions/search-readwise-highlights.md) | GET | Finds highlights in Readwise by semantic search. |
| [Set Reader Highlight Notes](actions/set-reader-highlight-notes.md) | PUT | Updates notes on a Readwise Reader highlight. |
| [Update Highlight](actions/update-highlight.md) | PUT | Updates an existing highlight in Readwise. |
| [Update Readwise Highlight With Tags](actions/update-readwise-highlight-with-tags.md) | PUT | Updates a Readwise highlight and its tags. |

### Highlight Tag

| Action | Method | Description |
| --- | --- | --- |
| [Add Highlight Tag](actions/add-highlight-tag.md) | POST | Creates a new tag for a Readwise highlight. |
| [Get Highlight Tag](actions/get-highlight-tag.md) | GET | Retrieves a tag from a Readwise highlight. |
| [Remove Highlight Tag](actions/remove-highlight-tag.md) | DELETE | Deletes a tag from a Readwise highlight. |
| [Update Highlight Tag](actions/update-highlight-tag.md) | PUT | Updates an existing tag on a Readwise highlight. |

### Reader Document

| Action | Method | Description |
| --- | --- | --- |
| [Add Tags To Reader Document](actions/add-tags-to-reader-document.md) | PUT | Adds tags to a document in Readwise Reader. |
| [Bulk Update Reader Documents](actions/bulk-update-reader-documents.md) | PUT | Updates multiple documents in Readwise Reader. |
| [Create Reader Document](actions/create-reader-document.md) | POST | Creates a new document in Readwise Reader. |
| [Delete Reader Document](actions/delete-reader-document.md) | DELETE | Deletes an existing document from Readwise Reader. |
| [Edit Reader Document Metadata](actions/edit-reader-document-metadata.md) | PUT | Updates metadata for documents in Readwise Reader. |
| [Get Reader Document](actions/get-reader-document.md) | GET | Retrieves a document from Readwise Reader. |
| [Get Reader Document Details](actions/get-reader-document-details.md) | GET | Retrieves detailed document information from Readwise Reader. |
| [List Reader Documents](actions/list-reader-documents.md) | GET | Retrieves documents from the Readwise Reader library. |
| [Move Reader Documents](actions/move-reader-documents.md) | PUT | Updates document locations in Readwise Reader. |
| [Remove Tags From Reader Document](actions/remove-tags-from-reader-document.md) | PUT | Removes tags from a document in Readwise Reader. |
| [Save Document To Reader](actions/save-document-to-reader.md) | POST | Saves a document to Readwise Reader. |
| [Search Reader Documents](actions/search-reader-documents.md) | GET | Finds documents in Readwise Reader by query. |
| [Update Reader Document](actions/update-reader-document.md) | PUT | Updates an existing document in Readwise Reader. |

### Reader Document Export

| Action | Method | Description |
| --- | --- | --- |
| [Export Reader Documents](actions/export-reader-documents.md) | GET | Starts a Readwise Reader document export. |
| [Get Reader Document Export Status](actions/get-reader-document-export-status.md) | GET | Retrieves a Readwise Reader export status. |

### Review

| Action | Method | Description |
| --- | --- | --- |
| [Get Daily Review](actions/get-daily-review.md) | GET | Retrieves the daily review from Readwise. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Book Tags](actions/list-book-tags.md) | GET | Retrieves tags for a Readwise book. |
| [List Highlight Tags](actions/list-highlight-tags.md) | GET | Retrieves tags for a Readwise highlight. |
| [List Reader Tags](actions/list-reader-tags.md) | GET | Retrieves tags from the Readwise Reader library. |

