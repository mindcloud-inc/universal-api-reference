# CrewMem: Native API Reference

A consolidated summary of CrewMem's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://crewmem.com/docs/api/
- **OpenAPI specification:** https://crewmem.com/swagger/doc.json
- **API base URL:** `https://crewmem.com`

## Authentication

### API Key

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://crewmem.com/api/v1/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 20). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Memory](actions/add-memory.md) | `POST /api/v1/memory/add` | [docs](https://crewmem.com/docs/api/) |
| [Create Member](actions/create-member.md) | `POST /api/v1/member/create` | [docs](https://crewmem.com/docs/api/) |
| [Create Memory](actions/create-memory.md) | `POST /api/v1/memory/create` | [docs](https://crewmem.com/docs/api/) |
| [Create Team](actions/create-team.md) | `POST /api/v1/team/create` | [docs](https://crewmem.com/docs/api/) |
| [Create Team Member](actions/create-team-member.md) | `POST /api/v1/team-member/create` | [docs](https://crewmem.com/docs/api/) |
| [Delete Member](actions/delete-member.md) | `POST /api/v1/member/delete` | [docs](https://crewmem.com/docs/api/) |
| [Delete Team](actions/delete-team.md) | `POST /api/v1/team/delete` | [docs](https://crewmem.com/docs/api/) |
| [Delete Team Member](actions/delete-team-member.md) | `POST /api/v1/team-member/delete` | [docs](https://crewmem.com/docs/api/) |
| [Get Memory Job](actions/get-memory-job.md) | `GET /api/memory/jobs/:id` | [docs](https://crewmem.com/docs/api/) |
| [List Memory Jobs](actions/list-memory-jobs.md) | `GET /api/memory/jobs` | [docs](https://crewmem.com/docs/api/) |
