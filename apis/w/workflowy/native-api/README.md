# Workflowy: Native API Reference

A consolidated summary of Workflowy's API configuration and 10 documented operations, with links to official documentation.

- **Official docs:** https://beta.workflowy.com/api-reference/
- **API base URL:** `https://workflowy.com/api/v1`

## Authentication

### API Key

Connect Workflowy with an API key generated from Workflowy settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://workflowy.com/learn/integrations/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (10 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Complete Node](actions/complete-node.md) | `POST /nodes/:id/complete` | [docs](https://beta.workflowy.com/api-reference/) |
| [Create Node](actions/create-node.md) | `POST /nodes` | [docs](https://beta.workflowy.com/api-reference/) |
| [Delete Node](actions/delete-node.md) | `DELETE /nodes/:id` | [docs](https://beta.workflowy.com/api-reference/) |
| [Export All Nodes](actions/export-all-nodes.md) | `GET /nodes-export` | [docs](https://beta.workflowy.com/api-reference/) |
| [List Nodes](actions/list-nodes.md) | `GET /nodes` | [docs](https://beta.workflowy.com/api-reference/) |
| [List Targets](actions/list-targets.md) | `GET /targets` | [docs](https://beta.workflowy.com/api-reference/) |
| [Move Node](actions/move-node.md) | `POST /nodes/:id/move` | [docs](https://beta.workflowy.com/api-reference/) |
| [Retrieve Node](actions/retrieve-node.md) | `GET /nodes/:id` | [docs](https://beta.workflowy.com/api-reference/) |
| [Uncomplete Node](actions/uncomplete-node.md) | `POST /nodes/:id/uncomplete` | [docs](https://beta.workflowy.com/api-reference/) |
| [Update Node](actions/update-node.md) | `POST /nodes/:id` | [docs](https://beta.workflowy.com/api-reference/) |
