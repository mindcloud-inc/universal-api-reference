# <img src="https://images.mindcloud.co/apps/icons/notion-logo_1773337117577.png" alt="Notion logo" width="28" height="28"> Notion: Universal API

Write docs, organize projects, manage knowledge, and collaborate with teams.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/notion/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 27
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.notion.so
- **Vendor API docs:** https://developers.notion.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve Bot User](actions/retrieve-bot-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/notion/latest/actions/retrieve-bot-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (27)

### Data Source

| Action | Method | Description |
| --- | --- | --- |
| [Create Data Source](actions/create-data-source.md) | POST |  |
| [Update Data Source](actions/update-data-source.md) | PUT |  |

### Database

| Action | Method | Description |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | POST |  |
| [Update Database](actions/update-database.md) | PUT |  |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Append Block Children](actions/append-block-children.md) | PUT | Appends child blocks to a Notion block. |
| [Complete File Upload](actions/complete-file-upload.md) | PUT | Finalizes a file upload in Notion. |
| [Create Comment](actions/create-comment.md) | POST | Creates a new comment in Notion. |
| [Create File Upload](actions/create-file-upload.md) | POST | Initiates a new file upload in Notion. |
| [Create Page](actions/create-page.md) | POST | Creates a new page in Notion. |
| [Delete Block](actions/delete-block.md) | DELETE | Deletes an existing block from Notion. |
| [List Block Children](actions/list-block-children.md) | GET | Retrieves child blocks for a Notion block. |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments from the connected Notion workspace. |
| [List Data Source Templates](actions/list-data-source-templates.md) | GET | Retrieves page templates for a Notion data source. |
| [Query Data Source](actions/query-data-source.md) | GET | Retrieves filtered records from a Notion data source. |
| [Retrieve Block](actions/retrieve-block.md) | GET | Retrieves details for a block from Notion. |
| [Retrieve Data Source](actions/retrieve-data-source.md) | GET | Retrieves a data source from Notion. |
| [Retrieve Data Source Template](actions/retrieve-data-source-template.md) | GET | Retrieves a data source template page from Notion. |
| [Retrieve Database (Compatibility)](actions/retrieve-database-compatibility.md) | GET | Retrieves a database from Notion's compatibility endpoint. |
| [Retrieve Page](actions/retrieve-page.md) | GET | Retrieves details for a page from Notion. |
| [Retrieve Page Property Item](actions/retrieve-page-property-item.md) | GET | Retrieves a page property item from Notion. |
| [Search](actions/search.md) | GET | Finds pages and data sources in Notion by title. |
| [Send File Upload](actions/send-file-upload.md) | PUT | Sends file contents to a Notion upload. |
| [Update Block](actions/update-block.md) | PUT | Updates an existing block in Notion. |
| [Update Page](actions/update-page.md) | PUT | Updates an existing page in Notion. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from the connected Notion workspace. |
| [Retrieve Bot User](actions/retrieve-bot-user.md) | GET | Retrieves the current bot user from Notion. |
| [Retrieve User](actions/retrieve-user.md) | GET | Retrieves a user from the connected Notion workspace. |

