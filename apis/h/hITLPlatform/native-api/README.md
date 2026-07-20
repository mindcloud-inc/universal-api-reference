# HITL Platform: Native API Reference

A consolidated summary of HITL Platform's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://docs.hitl.sh/
- **API base URL:** `https://api.hitl.sh/v1`

## Authentication

### API Key

Use a HITL.sh API key in the Authorization bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.hitl.sh/api-keys)

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Request Feedback](actions/add-request-feedback.md) | `POST /api/requests/:id/feedback` | [docs](https://docs.hitl.sh/api-reference/requests/add-feedback) |
| [Cancel Request](actions/cancel-request.md) | `DELETE /api/requests/:id` | [docs](https://docs.hitl.sh/api-reference/requests/cancel-request) |
| [Create Loop](actions/create-loop.md) | `POST /api/loops` | [docs](https://docs.hitl.sh/api-reference/loops/create-loop) |
| [Create Request](actions/create-request.md) | `POST /api/loops/:loopId/requests` | [docs](https://docs.hitl.sh/api-reference/requests/create-request) |
| [Delete Loop](actions/delete-loop.md) | `DELETE /api/loops/:id` | [docs](https://docs.hitl.sh/api-reference/loops/delete-loop) |
| [Get Loop](actions/get-loop.md) | `GET /api/loops/:id` | [docs](https://docs.hitl.sh/api-reference/loops/get-loop) |
| [Get Request](actions/get-request.md) | `GET /api/requests/:id` | [docs](https://docs.hitl.sh/api-reference/requests/get-request) |
| [List Loop Members](actions/list-loop-members.md) | `GET /api/loops/:id/members` | [docs](https://docs.hitl.sh/concepts/loops) |
| [List Loop Requests](actions/list-loop-requests.md) | `GET /api/loops/:loopId/requests` | [docs](https://docs.hitl.sh/api-reference/introduction) |
| [List Loops](actions/list-loops.md) | `GET /api/loops` | [docs](https://docs.hitl.sh/api-reference/loops/get-loops) |
| [List Requests](actions/list-requests.md) | `GET /api/requests` | [docs](https://docs.hitl.sh/api-reference/requests/get-requests) |
| [Remove Loop Member](actions/remove-loop-member.md) | `DELETE /api/loops/:id/members/:userId` | [docs](https://docs.hitl.sh/api-reference/introduction) |
| [Test API Key](actions/test-api-key.md) | `GET /test` | [docs](https://docs.hitl.sh/api-keys) |
| [Update Loop](actions/update-loop.md) | `PUT /api/loops/:id` | [docs](https://docs.hitl.sh/api-reference/loops/update-loop) |
