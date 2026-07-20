# Paradym: Native API Reference

A consolidated summary of Paradym's API configuration and 29 documented operations, with links to official documentation.

- **Official docs:** https://paradym.id/reference
- **OpenAPI specification:** https://api.paradym.id/openapi.json
- **API base URL:** `https://api.paradym.id/v1`

## Authentication

### API Key

Connect with a Paradym API key and project ID.

### Credentials

- **API Key:** `apiKey` · required
- **Project ID:** `projectId` · required · Paradym project ID used by project-scoped endpoints.

Send these headers with each API request:

```http
x-access-token: <apiKey>
```

[Official authentication documentation](https://docs.paradym.id/api-and-dashboard/quickstart)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `page[size]` in the query string to set the page size (default 25; maximum 100). Use `page[after]` in the query string as the pagination cursor.

## Sorting

Set the sort field with `sort` in the query string. Prefix the field name to select its direction. Only one sort field is accepted.

## Endpoints (29 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Mdoc Credential Template](actions/archive-mdoc-credential-template.md) | `DELETE /projects/:projectId/templates/credentials/mdoc/:credentialTemplateId` | [docs](https://paradym.id/reference#tag/mdoc-credential-templates) |
| [Archive Presentation Template](actions/archive-presentation-template.md) | `DELETE /projects/:projectId/templates/presentations/:presentationTemplateId` | [docs](https://paradym.id/reference#tag/presentation-templates) |
| [Archive Sd-Jwt Vc Credential Template](actions/archive-sd-jwt-vc-credential-template.md) | `DELETE /projects/:projectId/templates/credentials/sd-jwt-vc/:credentialTemplateId` | [docs](https://paradym.id/reference#tag/sd-jwt-vc-credential-templates) |
| [Batch Revoke Credentials](actions/batch-revoke-credentials.md) | `POST /projects/:projectId/revocation/batch` | [docs](https://paradym.id/reference#tag/revocation) |
| [Create Certificate](actions/create-certificate.md) | `POST /projects/:projectId/certificates` | [docs](https://paradym.id/reference#tag/certificates) |
| [Create Mdoc Credential Template](actions/create-mdoc-credential-template.md) | `POST /projects/:projectId/templates/credentials/mdoc` | [docs](https://paradym.id/reference#tag/mdoc-credential-templates) |
| [Create Presentation Template](actions/create-presentation-template.md) | `POST /projects/:projectId/templates/presentations` | [docs](https://paradym.id/reference#tag/presentation-templates) |
| [Create Sd-Jwt Vc Credential Template](actions/create-sd-jwt-vc-credential-template.md) | `POST /projects/:projectId/templates/credentials/sd-jwt-vc` | [docs](https://paradym.id/reference#tag/sd-jwt-vc-credential-templates) |
| [Create Webhook](actions/create-webhook.md) | `POST /projects/:projectId/webhooks` | [docs](https://paradym.id/reference#tag/webhooks) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /projects/:projectId/webhooks/:webhookId` | [docs](https://paradym.id/reference#tag/webhooks) |
| [List Certificates](actions/list-certificates.md) | `GET /projects/:projectId/certificates` | [docs](https://paradym.id/reference#tag/certificates) |
| [List DIDs](actions/list-dids.md) | `GET /projects/:projectId/dids` | [docs](https://paradym.id/reference#tag/dids) |
| [List Issued Credentials](actions/list-issued-credentials.md) | `GET /projects/:projectId/issuance` | [docs](https://paradym.id/reference#tag/issued-credentials) |
| [List Mdoc Credential Templates](actions/list-mdoc-credential-templates.md) | `GET /projects/:projectId/templates/credentials/mdoc` | [docs](https://paradym.id/reference#tag/mdoc-credential-templates) |
| [List Presentation Templates](actions/list-presentation-templates.md) | `GET /projects/:projectId/templates/presentations` | [docs](https://paradym.id/reference#tag/presentation-templates) |
| [List Project Members](actions/list-project-members.md) | `GET /projects/:projectId/members` | [docs](https://paradym.id/reference#tag/projects) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://paradym.id/reference#tag/projects) |
| [List Sd-Jwt Vc Credential Templates](actions/list-sd-jwt-vc-credential-templates.md) | `GET /projects/:projectId/templates/credentials/sd-jwt-vc` | [docs](https://paradym.id/reference#tag/sd-jwt-vc-credential-templates) |
| [List Trusted Entities](actions/list-trusted-entities.md) | `GET /projects/:projectId/trusted-entities` | [docs](https://paradym.id/reference#tag/trusted-entities) |
| [List Webhooks](actions/list-webhooks.md) | `GET /projects/:projectId/webhooks` | [docs](https://paradym.id/reference#tag/webhooks) |
| [Retrieve Default Profile](actions/retrieve-default-profile.md) | `GET /projects/:projectId/profiles/default` | [docs](https://paradym.id/reference#tag/project-profile) |
| [Retrieve Mdoc Credential Template](actions/retrieve-mdoc-credential-template.md) | `GET /projects/:projectId/templates/credentials/mdoc/:credentialTemplateId` | [docs](https://paradym.id/reference#tag/mdoc-credential-templates) |
| [Retrieve Mdoc Credential Template JSON Schema](actions/retrieve-mdoc-credential-template-json-schema.md) | `GET /projects/:projectId/templates/credentials/mdoc/:credentialTemplateId/json-schema` | [docs](https://paradym.id/reference#tag/mdoc-credential-templates) |
| [Retrieve Presentation Template](actions/retrieve-presentation-template.md) | `GET /projects/:projectId/templates/presentations/:presentationTemplateId` | [docs](https://paradym.id/reference#tag/presentation-templates) |
| [Retrieve Sd-Jwt Vc Credential Template](actions/retrieve-sd-jwt-vc-credential-template.md) | `GET /projects/:projectId/templates/credentials/sd-jwt-vc/:credentialTemplateId` | [docs](https://paradym.id/reference#tag/sd-jwt-vc-credential-templates) |
| [Update Default Profile](actions/update-default-profile.md) | `PUT /projects/:projectId/profiles/default` | [docs](https://paradym.id/reference#tag/project-profile) |
| [Update Mdoc Credential Template](actions/update-mdoc-credential-template.md) | `PUT /projects/:projectId/templates/credentials/mdoc/:credentialTemplateId` | [docs](https://paradym.id/reference#tag/mdoc-credential-templates) |
| [Update Presentation Template](actions/update-presentation-template.md) | `PUT /projects/:projectId/templates/presentations/:presentationTemplateId` | [docs](https://paradym.id/reference#tag/presentation-templates) |
| [Update Project](actions/update-project.md) | `POST /projects/:projectId` | [docs](https://paradym.id/reference#tag/projects) |
