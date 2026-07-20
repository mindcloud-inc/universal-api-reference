# LinkAce: Native API Reference

A consolidated summary of LinkAce's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.linkace.org/
- **OpenAPI specification:** https://raw.githubusercontent.com/Kovah/LinkAce-API-Docs/main/openapi/LinkAce-API.v2.yaml
- **API base URL:** `https://demo.linkace.org/api/v2`

## Authentication

### API Token

Authenticate to LinkAce with a user API token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.linkace.org/docs/v2/configuration/user-api-tokens/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `User-Agent` | `Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/124.0.0.0 Safari/537.36` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size (minimum -1). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `order_by` in the query string. Set the direction separately with `order_dir`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Delete Links](actions/bulk-delete-links.md) | `DELETE /bulk/delete` | [docs](https://api-docs.linkace.org/#tag/Bulk/operation/post-api-v2-bulk-deletion) |
| [Bulk Edit Links](actions/bulk-edit-links.md) | `PATCH /bulk/links` | [docs](https://api-docs.linkace.org/#tag/Bulk/operation/patch-api-v2-bulk-links) |
| [Bulk Store Links](actions/bulk-store-links.md) | `POST /bulk/links` | [docs](https://api-docs.linkace.org/#tag/Bulk/operation/post-api-v2-bulk-links) |
| [Clear Trash](actions/clear-trash.md) | `DELETE /trash/clear` | [docs](https://api-docs.linkace.org/#tag/Trash/operation/delete-api-v2-trash-clear) |
| [Create Link](actions/create-link.md) | `POST /links` | [docs](https://api-docs.linkace.org/#tag/Links/operation/post-api-v2-links) |
| [Create List](actions/create-list.md) | `POST /lists` | [docs](https://api-docs.linkace.org/#tag/Lists/operation/post-api-v2-lists) |
| [Create Note](actions/create-note.md) | `POST /notes` | [docs](https://api-docs.linkace.org/#tag/Notes/operation/post-api-v2-notes) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://api-docs.linkace.org/#tag/Tags/operation/post-api-v2-tags) |
| [Delete Link](actions/delete-link.md) | `DELETE /links/{link_id}` | [docs](https://api-docs.linkace.org/#tag/Links/operation/delete-api-v2-links-link_id) |
| [Delete List](actions/delete-list.md) | `DELETE /lists/{list_id}` | [docs](https://api-docs.linkace.org/#tag/Lists/operation/delete-api-v2-lists-list_id) |
| [Delete Note](actions/delete-note.md) | `DELETE /notes/{note_id}` | [docs](https://api-docs.linkace.org/#tag/Notes/operation/delete-api-v2-notes-note_id) |
| [Delete Tag](actions/delete-tag.md) | `DELETE /tags/{tag_id}` | [docs](https://api-docs.linkace.org/#tag/Tags/operation/delete-api-v2-tags-tag_id) |
| [Get Link](actions/get-link.md) | `GET /links/{link_id}` | [docs](https://api-docs.linkace.org/#tag/Links/operation/get-api-v2-links-link_id) |
| [Get List](actions/get-list.md) | `GET /lists/{list_id}` | [docs](https://api-docs.linkace.org/#tag/Lists/operation/get-api-v2-lists-list_id) |
| [Get Tag](actions/get-tag.md) | `GET /tags/{tag_id}` | [docs](https://api-docs.linkace.org/#tag/Tags/operation/get-api-v2-tags-tag_id) |
| [List Links](actions/list-links.md) | `GET /links` | [docs](https://api-docs.linkace.org/#tag/Links/operation/get-api-v2-links) |
| [List Links for List](actions/list-links-for-list.md) | `GET /lists/{list_id}/links` | [docs](https://api-docs.linkace.org/#tag/Lists/operation/get-api-v2-lists-list_id-links) |
| [List Links for Tag](actions/list-links-for-tag.md) | `GET /tags/{tag_id}/links` | [docs](https://api-docs.linkace.org/#tag/Tags/operation/get-api-v2-tags-tag_id-links) |
| [List Lists](actions/list-lists.md) | `GET /lists` | [docs](https://api-docs.linkace.org/#tag/Lists/operation/get-api-v2-lists) |
| [List Notes for Link](actions/list-notes-for-link.md) | `GET /links/{link_id}/notes` | [docs](https://api-docs.linkace.org/#tag/Notes/operation/get-api-v2-links-link_id-notes) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://api-docs.linkace.org/#tag/Tags/operation/get-api-v2-tags) |
| [List Trash Links](actions/list-trash-links.md) | `GET /trash/links` | [docs](https://api-docs.linkace.org/#tag/Trash/operation/get-api-v2-trash-links) |
| [Restore Trash Entry](actions/restore-trash-entry.md) | `PATCH /trash/restore` | [docs](https://api-docs.linkace.org/#tag/Trash/operation/patch-api-v2-trash-restore) |
| [Search Links](actions/search-links.md) | `GET /search/links` | [docs](https://api-docs.linkace.org/#tag/Search/operation/get-api-v2-search-links) |
| [Search Lists](actions/search-lists.md) | `GET /search/lists` | [docs](https://api-docs.linkace.org/#tag/Search/operation/get-api-v2-search-lists) |
| [Search Tags](actions/search-tags.md) | `GET /search/tags` | [docs](https://api-docs.linkace.org/#tag/Search/operation/get-api-v2-search-tags) |
| [Update Link](actions/update-link.md) | `PATCH /links/{link_id}` | [docs](https://api-docs.linkace.org/#tag/Links/operation/patch-api-v2-links-link_id) |
| [Update List](actions/update-list.md) | `PATCH /lists/{list_id}` | [docs](https://api-docs.linkace.org/#tag/Lists/operation/patch-api-v2-lists-list_id) |
| [Update Note](actions/update-note.md) | `PATCH /notes/{note_id}` | [docs](https://api-docs.linkace.org/#tag/Notes/operation/patch-api-v2-notes-note_id) |
| [Update Tag](actions/update-tag.md) | `PATCH /tags/{tag_id}` | [docs](https://api-docs.linkace.org/#tag/Tags/operation/patch-api-v2-tags-tag_id) |
