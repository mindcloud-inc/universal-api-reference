# AppWright: Native API Reference

A consolidated summary of AppWright's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://docs.google.com/document/d/15cwpi-qdWiPcsSMziG8V41RzlJLw4yNqg0N0h_Em7xA/edit?tab=t.0
- **API base URL:** `https://{clientId}.AppWright.com`

## Authentication

### Custom

### Credentials

- **User:** `user` · required
- **Password:** `password` · required
- **Client Id:** `clientId` · required

Send these headers with each API request:

```http
AWAPI-PW: <password>
AWAPI-USER: <user>
```

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json; charset=utf-8` |

## Endpoints (3 documented)

| Operation | Method & path |
| --- | --- |
| [Create Job](actions/create-job.md) | `POST awAPI/awAPI.asp` |
| [Search SQL](actions/search-sql.md) | `POST awAPI/awAPI.asp` |
| [Update Task Date](actions/update-task-date.md) | `POST awAPI/awAPI.asp` |
