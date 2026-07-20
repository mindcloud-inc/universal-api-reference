# Leap AI: Native API Reference

A consolidated summary of Leap AI's API configuration and 2 documented operations, with links to official documentation.

- **Official docs:** https://docs.tryleap.ai/api-reference/getting-started
- **OpenAPI specification:** https://api.workflows.tryleap.ai/api-json
- **API base URL:** `https://api.workflows.tryleap.ai`

## Authentication

### API Key

Use a Leap Workflows API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
X-Api-Key: <apiKey>
```

[Official authentication documentation](https://docs.tryleap.ai/api-reference/getting-started)

## Endpoints (2 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Workflow Run](actions/get-workflow-run.md) | `GET /v2/runs/:workflowRunId` | [docs](https://docs.tryleap.ai/api-reference/get-workflow-run) |
| [Run Workflow](actions/run-workflow.md) | `POST /v2/runs` | [docs](https://docs.tryleap.ai/api-reference/run-workflow) |
