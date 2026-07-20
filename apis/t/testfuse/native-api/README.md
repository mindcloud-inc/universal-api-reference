# Testfuse: Native API Reference

A consolidated summary of Testfuse's API configuration and 3 documented operations, with links to official documentation.

- **Official docs:** https://api.testfuse.com
- **OpenAPI specification:** https://api.testfuse.com/openapi.json
- **API base URL:** `https://gateway.testfuse.com`

## Authentication

### Bearer Token

Connect to Testfuse with a bearer API token sent in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://api.testfuse.com)

## Endpoints (3 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Invite Candidates](actions/invite-candidates.md) | `POST /v1/users/invite_multiple_candidates` | [docs](https://api.testfuse.com) |
| [List Assessment Specs](actions/list-assessment-specs.md) | `GET /v1/assess_specs/` | [docs](https://api.testfuse.com) |
| [List Assessments](actions/list-assessments.md) | `GET /v1/assessments/` | [docs](https://api.testfuse.com) |
