# Gutendex: Universal API

Public JSON API for Project Gutenberg ebook metadata and catalog search via Gutendex.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gutendex/latest
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gutendex.com/
- **Vendor API docs:** https://gutendex.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Book](actions/get-book.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gutendex/latest/actions/get-book?connectionId=$CONNECTION_ID&bookId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Book

| Action | Method | Description |
| --- | --- | --- |
| [Get Book](actions/get-book.md) | GET | Retrieves book details from Gutendex. |
| [List Books](actions/list-books.md) | GET | Retrieves books from Gutendex. |
| [List Books By Author End Year](actions/list-books-by-author-end-year.md) | GET | Finds books in Gutendex by author end year. |
| [List Books By Author Start Year](actions/list-books-by-author-start-year.md) | GET | Finds books in Gutendex by author start year. |
| [List Books By Author Year Range](actions/list-books-by-author-year-range.md) | GET | Finds books in Gutendex by author year range. |
| [List Books By Copyright Status](actions/list-books-by-copyright-status.md) | GET | Finds books in Gutendex by copyright status. |
| [List Books By IDs](actions/list-books-by-ids.md) | GET | Finds books in Gutendex by Project Gutenberg IDs. |
| [List Books By Languages](actions/list-books-by-languages.md) | GET | Finds books in Gutendex by language. |
| [List Books By MIME Type](actions/list-books-by-mime-type.md) | GET | Finds books in Gutendex by MIME type. |
| [List Books By Topic](actions/list-books-by-topic.md) | GET | Finds books in Gutendex by topic. |
| [List Copyrighted Books](actions/list-copyrighted-books.md) | GET | Retrieves copyrighted books from Gutendex. |
| [List Newest Books](actions/list-newest-books.md) | GET | Retrieves the newest books from Gutendex. |
| [List Oldest Books](actions/list-oldest-books.md) | GET | Retrieves the oldest books from Gutendex. |
| [List Public Domain Books](actions/list-public-domain-books.md) | GET | Retrieves public domain books from Gutendex. |
| [Search Books](actions/search-books.md) | GET | Finds books in Gutendex by title or author search. |

