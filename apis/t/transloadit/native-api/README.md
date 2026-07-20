# Transloadit: Native API Reference

A consolidated summary of Transloadit's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://transloadit.com/docs/api/
- **API base URL:** `https://api2.transloadit.com`

## Authentication

### Bearer Token

Use a pre-minted Transloadit bearer token. Paste the token value directly into the connection. MindCloud will send it as Authorization: Bearer <token>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://transloadit.com/docs/api/token-post/)

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Assembly](actions/cancel-assembly.md) | `DELETE /assemblies/:assemblyId` | [docs](https://transloadit.com/docs/api/assemblies-assembly-id-delete/) |
| [Create Assembly](actions/create-assembly.md) | `POST /assemblies` | [docs](https://transloadit.com/docs/api/assemblies-post/) |
| [Create Template](actions/create-template.md) | `POST /templates` | [docs](https://transloadit.com/docs/api/templates-post/) |
| [Create Template Credential](actions/create-template-credential.md) | `POST /template_credentials` | [docs](https://transloadit.com/docs/api/template-credentials-post/) |
| [Delete Template](actions/delete-template.md) | `DELETE /templates/:templateId` | [docs](https://transloadit.com/docs/api/templates-template-id-delete/) |
| [Delete Template Credential](actions/delete-template-credential.md) | `DELETE /template_credentials/:credentialsId` | [docs](https://transloadit.com/docs/api/template-credentials-credentials-id-or-name-delete/) |
| [Edit Template](actions/edit-template.md) | `PUT /templates/:templateId` | [docs](https://transloadit.com/docs/api/templates-template-id-put/) |
| [Edit Template Credential](actions/edit-template-credential.md) | `PUT /template_credentials/:credentialsId` | [docs](https://transloadit.com/docs/api/template-credentials-credentials-id-or-name-put/) |
| [List Assemblies](actions/list-assemblies.md) | `GET /assemblies` | [docs](https://transloadit.com/docs/api/assemblies-get/) |
| [List Template Credentials](actions/list-template-credentials.md) | `GET /template_credentials` | [docs](https://transloadit.com/docs/api/template-credentials-get/) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://transloadit.com/docs/api/templates-get/) |
| [Replay Assembly](actions/replay-assembly.md) | `POST /assemblies/:assemblyId/replay` | [docs](https://transloadit.com/docs/api/assemblies-assembly-id-replay-post/) |
| [Replay Assembly Notification](actions/replay-assembly-notification.md) | `POST /assembly_notifications/:assemblyId/replay` | [docs](https://transloadit.com/docs/api/assembly-notifications-assembly-id-replay-post/) |
| [Retrieve Assembly Status](actions/retrieve-assembly-status.md) | `GET /assemblies/:assemblyId` | [docs](https://transloadit.com/docs/api/assemblies-assembly-id-get/) |
| [Retrieve a month's bill](actions/retrieve-months-bill.md) | `GET /bill/:billDate` | [docs](https://transloadit.com/docs/api/bill-date-get/) |
| [Retrieve currently used priority job slots](actions/retrieve-priority-job-slots.md) | `GET /queues/job_slots` | [docs](https://transloadit.com/docs/api/queues-job-slots-get/) |
| [Retrieve Template](actions/retrieve-template.md) | `GET /templates/:templateId` | [docs](https://transloadit.com/docs/api/templates-template-id-get/) |
| [Retrieve Template Credential](actions/retrieve-template-credential.md) | `GET /template_credentials/:credentialsId` | [docs](https://transloadit.com/docs/api/template-credentials-credentials-id-or-name-get/) |
