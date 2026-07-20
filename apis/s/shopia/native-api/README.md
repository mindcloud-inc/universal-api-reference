# Shopia: Native API Reference

A consolidated summary of Shopia's API configuration and 1 documented operations, with links to official documentation.

- **Official docs:** https://docs.axelerate.ai/en/collections/8820825-integrations-api
- **API base URL:** `https://automation-run-1he1fvca.uc.gateway.dev`

## Authentication

### API Key

Current live runtime evidence shows this Shopia automation requires three connection values: the generated API key, the automation token, and the workflow identifier. The request succeeds when all three values are present in the automation URL query string.

### Credentials

- **API Key:** `apiKey` · required
- **Token:** `token` · required · The Shopia automation token from the working API snippet.
- **Workflow ID:** `workflowId` · required · The Shopia workflow identifier from the working API snippet.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.axelerate.ai/en/articles/9553232-using-the-automations-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Endpoints (1 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Generate Article Ideas](actions/generate-article-ideas.md) | `POST https://automation-run-1he1fvca.uc.gateway.dev/automation?key={{credentials.apiKey}}&token={{credentials.token}}&workflow={{credentials.workflowId}}` | [docs](https://docs.axelerate.ai/en/articles/9553232-using-the-automations-api) |
