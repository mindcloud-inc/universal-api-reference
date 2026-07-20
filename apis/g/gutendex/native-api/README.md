# Gutendex: Native API Reference

A consolidated summary of Gutendex's API configuration and 15 documented operations, with links to official documentation.

- **Official docs:** https://gutendex.com/
- **API base URL:** `https://gutendex.com`

## Authentication

### No Authentication

Gutendex publishes a public API and does not require authentication for the documented /books endpoints.

This API does not require request authentication.

[Official authentication documentation](https://gutendex.com/)

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Filtering

Send filters in the query string.

## Sorting

Set the sort field with `sort` in the query string. Only one sort field is accepted.

## Endpoints (15 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Book](actions/get-book.md) | `GET /books/:bookId/` |  |
| [List Books](actions/list-books.md) | `GET /books/` | [docs](https://gutendex.com/) |
| [List Books By Author End Year](actions/list-books-by-author-end-year.md) | `GET /books/` |  |
| [List Books By Author Start Year](actions/list-books-by-author-start-year.md) | `GET /books/` |  |
| [List Books By Author Year Range](actions/list-books-by-author-year-range.md) | `GET /books/` |  |
| [List Books By Copyright Status](actions/list-books-by-copyright-status.md) | `GET /books/` |  |
| [List Books By IDs](actions/list-books-by-ids.md) | `GET /books/` |  |
| [List Books By Languages](actions/list-books-by-languages.md) | `GET /books/` |  |
| [List Books By MIME Type](actions/list-books-by-mime-type.md) | `GET /books/` |  |
| [List Books By Topic](actions/list-books-by-topic.md) | `GET /books/` |  |
| [List Copyrighted Books](actions/list-copyrighted-books.md) | `GET /books/` |  |
| [List Newest Books](actions/list-newest-books.md) | `GET /books/` |  |
| [List Oldest Books](actions/list-oldest-books.md) | `GET /books/` |  |
| [List Public Domain Books](actions/list-public-domain-books.md) | `GET /books/` |  |
| [Search Books](actions/search-books.md) | `GET /books/` |  |
