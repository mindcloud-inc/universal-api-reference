# <img src="https://images.mindcloud.co/apps/icons/images-17_1776088062442.png" alt="Affinda logo" width="28" height="28"> Affinda: Universal API

Extract structured data from documents and manage Affinda workspaces, document types, documents, and webhooks.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/affinda/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.affinda.com/
- **Vendor API docs:** https://docs.affinda.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Organizations](actions/list-organizations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/affinda/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Annotation

| Action | Method | Description |
| --- | --- | --- |
| [Get specific annotation](actions/get-annotation.md) | GET | Retrieves a specific annotation from Affinda. |
| [Get list of all annotations](actions/list-annotations.md) | GET | Retrieves annotations for an Affinda document. |

### Data Source Value

| Action | Method | Description |
| --- | --- | --- |
| [Get specific data source value](actions/get-data-source-value.md) | GET | Retrieves a specific Affinda mapping data source value. |
| [List values for a data source](actions/list-data-source-values.md) | GET | Retrieves values from an Affinda mapping data source. |

### Data Sources

| Action | Method | Description |
| --- | --- | --- |
| [Get specific data source](actions/get-data-source.md) | GET | Retrieves a specific mapping data source from Affinda. |
| [List data sources](actions/list-data-sources.md) | GET | Retrieves custom mapping data sources from Affinda. |

### Document Type

| Action | Method | Description |
| --- | --- | --- |
| [Get a document type](actions/get-document-type.md) | GET | Retrieves a specific document type from Affinda. |
| [List document types](actions/list-document-types.md) | GET | Retrieves accessible document types from Affinda. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get specific document](actions/get-document.md) | GET | Retrieves a specific document from Affinda. |
| [Get redacted document](actions/get-redacted-document.md) | GET | Retrieves a redacted document from Affinda. |
| [Get list of all documents](actions/list-documents.md) | GET | Retrieves accessible document summaries from Affinda. |

### Extractor

| Action | Method | Description |
| --- | --- | --- |
| [Get specific extractor](actions/get-extractor.md) | GET | Retrieves a specific extractor from Affinda. |
| [Get list of all extractors](actions/list-extractors.md) | GET | Retrieves all accessible extractors from Affinda. |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List occupation groups](actions/list-occupation-groups.md) | GET | Retrieves searchable occupation groups from Affinda. |

### Invitations

| Action | Method | Description |
| --- | --- | --- |
| [Get list of all invitations](actions/list-invitations.md) | GET | Retrieves all accessible invitations from Affinda. |

### Json Schema

| Action | Method | Description |
| --- | --- | --- |
| [Generate JSON schema from a document type](actions/get-document-type-json-schema.md) | GET | Retrieves a JSON schema for an Affinda document type. |

### Memberships

| Action | Method | Description |
| --- | --- | --- |
| [Get specific workspace membership](actions/get-workspace-membership.md) | GET | Retrieves a specific workspace membership from Affinda. |
| [Get list of all workspace memberships](actions/list-workspace-memberships.md) | GET | Retrieves all workspace memberships from Affinda. |

### Organizations

| Action | Method | Description |
| --- | --- | --- |
| [Get detail of an organization](actions/get-organization.md) | GET | Retrieves a specific organization from Affinda. |
| [List Organizations](actions/list-organizations.md) | GET | Retrieves all accessible organizations from Affinda. |

### Pydantic Model

| Action | Method | Description |
| --- | --- | --- |
| [Generate Pydantic models from a document type](actions/get-document-type-pydantic-models.md) | GET | Retrieves Pydantic models for an Affinda document type. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get specific tag](actions/get-tag.md) | GET | Retrieves a specific tag from Affinda. |
| [Get list of all tags](actions/list-tags.md) | GET | Retrieves all accessible tags from Affinda. |

### Validation Result

| Action | Method | Description |
| --- | --- | --- |
| [Get specific validation result](actions/get-validation-result.md) | GET | Retrieves a specific validation result from Affinda. |
| [Get list of all validation results](actions/list-validation-results.md) | GET | Retrieves validation results for an Affinda document. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Get specific resthook subscription](actions/get-webhook.md) | GET | Retrieves a specific resthook subscription from Affinda. |
| [Get list of all resthook subscriptions](actions/list-webhooks.md) | GET | Retrieves all resthook subscriptions from Affinda. |

### Workspaces

| Action | Method | Description |
| --- | --- | --- |
| [Get specific workspace](actions/get-workspace.md) | GET | Retrieves a specific workspace from Affinda. |
| [Get usage by workspace](actions/get-workspace-usage.md) | GET | Retrieves monthly credits usage for an Affinda workspace. |
| [Get list of all workspaces](actions/list-workspaces.md) | GET | Retrieves all accessible workspaces from Affinda. |

