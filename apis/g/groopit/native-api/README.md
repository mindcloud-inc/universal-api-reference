# Groopit: Native API Reference

A consolidated summary of Groopit's API configuration and 4 documented operations, with links to official documentation.

- **Official docs:** https://groopit.co/help-center/tips-tricks/
- **API base URL:** `https://app.groopit.co/odata`

## Authentication

### API Key

Use a Groopit OData access token for the shared feed.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://groopit.co/help-center/tips-tricks/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `value`.

## Endpoints (4 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Assignment](actions/get-assignment.md) | `GET /Assignments(:assignmentId)` | [docs](https://3996879.fs1.hubspotusercontent-na1.net/hubfs/3996879/Knowledgebase/Groopit%20OData%20Instructions%209.2024.pdf) |
| [Get Assignment Post](actions/get-assignment-post.md) | `GET /Assignments(:assignmentId)/Posts(:postId)` | [docs](https://3996879.fs1.hubspotusercontent-na1.net/hubfs/3996879/Knowledgebase/Groopit%20OData%20Instructions%209.2024.pdf) |
| [List Assignment Posts](actions/list-assignment-posts.md) | `GET /Assignments(:assignmentId)/Posts` | [docs](https://3996879.fs1.hubspotusercontent-na1.net/hubfs/3996879/Knowledgebase/Groopit%20OData%20Instructions%209.2024.pdf) |
| [List Assignments](actions/list-assignments.md) | `GET /Assignments` | [docs](https://3996879.fs1.hubspotusercontent-na1.net/hubfs/3996879/Knowledgebase/Groopit%20OData%20Instructions%209.2024.pdf) |
