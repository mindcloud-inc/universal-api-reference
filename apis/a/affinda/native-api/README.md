# Affinda: Native API Reference

A consolidated summary of Affinda's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.affinda.com/
- **OpenAPI specification:** https://api.affinda.com/static/v3/api_spec.yaml
- **API base URL:** `https://api.us1.affinda.com`

## Authentication

### API Key

Connect with an Affinda API key using Bearer token authentication.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.affinda.com/)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get specific annotation](actions/get-annotation.md) | `GET /v3/annotations/:id` | [docs](https://docs.affinda.com/) |
| [Get specific data source](actions/get-data-source.md) | `GET /v3/mapping_data_sources/:identifier` | [docs](https://docs.affinda.com/) |
| [Get specific data source value](actions/get-data-source-value.md) | `GET /v3/mapping_data_sources/:identifier/values/:value` | [docs](https://docs.affinda.com/) |
| [Get specific document](actions/get-document.md) | `GET /v3/documents/:identifier` | [docs](https://docs.affinda.com/) |
| [Get a document type](actions/get-document-type.md) | `GET /v3/document_types/:identifier` | [docs](https://docs.affinda.com/) |
| [Generate JSON schema from a document type](actions/get-document-type-json-schema.md) | `GET /v3/document_types/:identifier/json_schema` | [docs](https://docs.affinda.com/) |
| [Generate Pydantic models from a document type](actions/get-document-type-pydantic-models.md) | `GET /v3/document_types/:identifier/pydantic_models` | [docs](https://docs.affinda.com/) |
| [Get specific extractor](actions/get-extractor.md) | `GET /v3/extractors/:identifier` | [docs](https://docs.affinda.com/) |
| [Get detail of an organization](actions/get-organization.md) | `GET /v3/organizations/:identifier` | [docs](https://docs.affinda.com/) |
| [Get redacted document](actions/get-redacted-document.md) | `GET /v3/documents/:identifier/redacted` | [docs](https://docs.affinda.com/) |
| [Get specific tag](actions/get-tag.md) | `GET /v3/tags/:id` | [docs](https://docs.affinda.com/) |
| [Get specific validation result](actions/get-validation-result.md) | `GET /v3/validation_results/:id` | [docs](https://docs.affinda.com/) |
| [Get specific resthook subscription](actions/get-webhook.md) | `GET /v3/resthook_subscriptions/:id` | [docs](https://docs.affinda.com/) |
| [Get specific workspace](actions/get-workspace.md) | `GET /v3/workspaces/:identifier` | [docs](https://docs.affinda.com/) |
| [Get specific workspace membership](actions/get-workspace-membership.md) | `GET /v3/workspace_memberships/:identifier` | [docs](https://docs.affinda.com/) |
| [Get usage by workspace](actions/get-workspace-usage.md) | `GET /v3/workspaces/:identifier/usage` | [docs](https://docs.affinda.com/) |
| [Get list of all annotations](actions/list-annotations.md) | `GET /v3/annotations` | [docs](https://docs.affinda.com/) |
| [List values for a data source](actions/list-data-source-values.md) | `GET /v3/mapping_data_sources/:identifier/values` | [docs](https://docs.affinda.com/) |
| [List data sources](actions/list-data-sources.md) | `GET /v3/mapping_data_sources` | [docs](https://docs.affinda.com/) |
| [List document types](actions/list-document-types.md) | `GET /v3/document_types` | [docs](https://docs.affinda.com/) |
| [Get list of all documents](actions/list-documents.md) | `GET /v3/documents` | [docs](https://docs.affinda.com/) |
| [Get list of all extractors](actions/list-extractors.md) | `GET /v3/extractors` | [docs](https://docs.affinda.com/) |
| [Get list of all invitations](actions/list-invitations.md) | `GET /v3/invitations` | [docs](https://docs.affinda.com/) |
| [List occupation groups](actions/list-occupation-groups.md) | `GET /v3/occupation_groups` | [docs](https://docs.affinda.com/) |
| [List Organizations](actions/list-organizations.md) | `GET /v3/organizations` | [docs](https://docs.affinda.com/api-reference/organizations/get-list-of-all-organizations) |
| [Get list of all tags](actions/list-tags.md) | `GET /v3/tags` | [docs](https://docs.affinda.com/) |
| [Get list of all validation results](actions/list-validation-results.md) | `GET /v3/validation_results` | [docs](https://docs.affinda.com/) |
| [Get list of all resthook subscriptions](actions/list-webhooks.md) | `GET /v3/resthook_subscriptions` | [docs](https://docs.affinda.com/) |
| [Get list of all workspace memberships](actions/list-workspace-memberships.md) | `GET /v3/workspace_memberships` | [docs](https://docs.affinda.com/) |
| [Get list of all workspaces](actions/list-workspaces.md) | `GET /v3/workspaces` | [docs](https://docs.affinda.com/) |
