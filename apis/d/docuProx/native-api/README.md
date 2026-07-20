# DocuProx: Native API Reference

A consolidated summary of DocuProx's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://docuprox.com/docs/api/
- **API base URL:** `https://api.docuprox.com`

## Authentication

### API Key

Authenticate DocuProx API requests with your API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-auth: <apiKey>
```

[Official authentication documentation](https://docuprox.com/docs/getting-started/)

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Processing Job](actions/create-processing-job.md) | `POST /v1/process-job` | [docs](https://docuprox.com/docs/api/#process-job-endpoint) |
| [Get Job Status](actions/get-job-status.md) | `GET /v1/job-status` | [docs](https://docuprox.com/docs/api/#job-status-endpoint) |
| [Process Document](actions/process-document.md) | `POST /v1/process` | [docs](https://docuprox.com/docs/api/#process-endpoint) |
| [Process Document Binary Upload](actions/process-document-binary-upload.md) | `PUT /v1/process` | [docs](https://docuprox.com/docs/api/#process-endpoint) |
| [Process Document with Agent](actions/process-document-with-agent.md) | `POST /v1/process-agent` | [docs](https://docuprox.com/docs/api/#process-agent-endpoint) |
| [Retrieve Job Results](actions/retrieve-job-results.md) | `POST /v1/job-results` | [docs](https://docuprox.com/docs/api/#job-results-endpoint) |
