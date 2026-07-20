# Copper: Native API Reference

A consolidated summary of Copper's API configuration, with links to official documentation.

- **Official docs:** https://developer.copper.com/
- **API base URL:** `https://api.copper.com/developer_api/v1`

## Authentication

### Custom Header Auth

Connect with a Copper API key and user email sent as Copper headers.

### Credentials

- **API Key:** `apiKey` · required · Copper API key generated in Copper System settings.
- **User Email:** `userEmail` · required · Email address of the Copper user who generated the API key.

Send these headers with each API request:

```http
X-PW-UserEmail: <userEmail>
X-PW-AccessToken: <apiKey>
```

[Official authentication documentation](https://developer.copper.com/introduction/authentication.html)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `page_size` in the request body to set the page size (default 25). Use `page_number` in the request body to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the request body. Set the direction separately with `sort_direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.
