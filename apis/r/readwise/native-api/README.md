# Readwise: Native API Reference

A consolidated summary of Readwise's API configuration and 43 documented operations, with links to official documentation.

- **Official docs:** https://readwise.io/reader_api
- **API base URL:** `https://readwise.io`

## Authentication

### Access Token

Use your Readwise access token. Readwise expects requests to send Authorization: Token <access_token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://readwise.io/access_token)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 100; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (43 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Book Tag](actions/add-book-tag.md) | `POST /api/v2/books/:bookId/tags/` | [docs](https://readwise.io/api_deets) |
| [Add Highlight Tag](actions/add-highlight-tag.md) | `POST /api/v2/highlights/:highlightId/tags/` | [docs](https://readwise.io/api_deets) |
| [Add Tags To Reader Document](actions/add-tags-to-reader-document.md) | `POST https://mcp2.readwise.io/mcp` | [docs](https://github.com/readwiseio/readwise-cli) |
| [Add Tags To Reader Highlight](actions/add-tags-to-reader-highlight.md) | `POST https://mcp2.readwise.io/mcp` | [docs](https://github.com/readwiseio/readwise-cli) |
| [Bulk Update Reader Documents](actions/bulk-update-reader-documents.md) | `PATCH /api/v3/bulk_update/` | [docs](https://readwise.io/reader_api) |
| [Create Highlights](actions/create-highlights.md) | `POST /api/v2/highlights/` | [docs](https://readwise.io/api_deets) |
| [Create Reader Document](actions/create-reader-document.md) | `POST https://mcp2.readwise.io/mcp` | [docs](https://github.com/readwiseio/readwise-cli) |
| [Create Reader Highlight](actions/create-reader-highlight.md) | `POST https://mcp2.readwise.io/mcp` | [docs](https://github.com/readwiseio/readwise-cli) |
| [Delete Highlight](actions/delete-highlight.md) | `DELETE /api/v2/highlights/:highlightId/` | [docs](https://readwise.io/api_deets) |
| [Delete Reader Document](actions/delete-reader-document.md) | `DELETE /api/v3/delete/:documentId/` | [docs](https://readwise.io/reader_api) |
| [Edit Reader Document Metadata](actions/edit-reader-document-metadata.md) | `POST https://mcp2.readwise.io/mcp` | [docs](https://github.com/readwiseio/readwise-cli) |
| [Export Highlights](actions/export-highlights.md) | `GET /api/v2/export/` | [docs](https://readwise.io/api_deets) |
| [Export Reader Documents](actions/export-reader-documents.md) | `POST https://mcp2.readwise.io/mcp` | [docs](https://github.com/readwiseio/readwise-cli) |
| [Get Book](actions/get-book.md) | `GET /api/v2/books/:book_id/` | [docs](https://readwise.io/api_deets) |
| [Get Book Tag](actions/get-book-tag.md) | `GET /api/v2/books/:bookId/tags/:tagId` | [docs](https://readwise.io/api_deets) |
| [Get Daily Review](actions/get-daily-review.md) | `GET /api/v2/review/` | [docs](https://readwise.io/api_deets) |
| [Get Highlight](actions/get-highlight.md) | `GET /api/v2/highlights/:highlight_id/` | [docs](https://readwise.io/api_deets) |
| [Get Highlight Tag](actions/get-highlight-tag.md) | `GET /api/v2/highlights/:highlightId/tags/:tagId` | [docs](https://readwise.io/api_deets) |
| [Get Reader Document](actions/get-reader-document.md) | `GET /api/v3/list/` | [docs](https://readwise.io/reader_api) |
| [Get Reader Document Details](actions/get-reader-document-details.md) | `POST https://mcp2.readwise.io/mcp` | [docs](https://github.com/readwiseio/readwise-cli) |
| [Get Reader Document Export Status](actions/get-reader-document-export-status.md) | `POST https://mcp2.readwise.io/mcp` | [docs](https://github.com/readwiseio/readwise-cli) |
| [Get Reader Document Highlights](actions/get-reader-document-highlights.md) | `POST https://mcp2.readwise.io/mcp` | [docs](https://github.com/readwiseio/readwise-cli) |
| [List Book Tags](actions/list-book-tags.md) | `GET /api/v2/books/:book_id/tags` | [docs](https://readwise.io/api_deets) |
| [List Books](actions/list-books.md) | `GET /api/v2/books/` | [docs](https://readwise.io/api_deets) |
| [List Highlight Tags](actions/list-highlight-tags.md) | `GET /api/v2/highlights/:highlight_id/tags` | [docs](https://readwise.io/api_deets) |
| [List Highlights](actions/list-highlights.md) | `GET /api/v2/highlights/` | [docs](https://readwise.io/api_deets) |
| [List Reader Documents](actions/list-reader-documents.md) | `GET /api/v3/list/` | [docs](https://readwise.io/reader_api) |
| [List Reader Tags](actions/list-reader-tags.md) | `GET /api/v3/tags/` | [docs](https://readwise.io/reader_api) |
| [Move Reader Documents](actions/move-reader-documents.md) | `POST https://mcp2.readwise.io/mcp` | [docs](https://github.com/readwiseio/readwise-cli) |
| [Remove Book Tag](actions/remove-book-tag.md) | `DELETE /api/v2/books/:bookId/tags/:tagId` | [docs](https://readwise.io/api_deets) |
| [Remove Highlight Tag](actions/remove-highlight-tag.md) | `DELETE /api/v2/highlights/:highlightId/tags/:tagId` | [docs](https://readwise.io/api_deets) |
| [Remove Tags From Reader Document](actions/remove-tags-from-reader-document.md) | `POST https://mcp2.readwise.io/mcp` | [docs](https://github.com/readwiseio/readwise-cli) |
| [Remove Tags From Reader Highlight](actions/remove-tags-from-reader-highlight.md) | `POST https://mcp2.readwise.io/mcp` | [docs](https://github.com/readwiseio/readwise-cli) |
| [Save Document To Reader](actions/save-document-to-reader.md) | `POST /api/v3/save/` | [docs](https://readwise.io/reader_api) |
| [Search Reader Documents](actions/search-reader-documents.md) | `POST https://mcp2.readwise.io/mcp` | [docs](https://github.com/readwiseio/readwise-cli) |
| [Search Readwise Highlights](actions/search-readwise-highlights.md) | `POST https://mcp2.readwise.io/mcp` | [docs](https://github.com/readwiseio/readwise-cli) |
| [Set Reader Highlight Notes](actions/set-reader-highlight-notes.md) | `POST https://mcp2.readwise.io/mcp` | [docs](https://github.com/readwiseio/readwise-cli) |
| [Update Book Tag](actions/update-book-tag.md) | `PATCH /api/v2/books/:bookId/tags/:tagId` | [docs](https://readwise.io/api_deets) |
| [Update Highlight](actions/update-highlight.md) | `PATCH /api/v2/highlights/:highlightId/` | [docs](https://readwise.io/api_deets) |
| [Update Highlight Tag](actions/update-highlight-tag.md) | `PATCH /api/v2/highlights/:highlightId/tags/:tagId` | [docs](https://readwise.io/api_deets) |
| [Update Reader Document](actions/update-reader-document.md) | `PATCH /api/v3/update/:documentId/` | [docs](https://readwise.io/reader_api) |
| [Update Readwise Highlight With Tags](actions/update-readwise-highlight-with-tags.md) | `POST https://mcp2.readwise.io/mcp` | [docs](https://github.com/readwiseio/readwise-cli) |
| [Validate Connection](actions/validate-connection.md) | `GET /api/v2/auth/` | [docs](https://readwise.io/api_deets) |
