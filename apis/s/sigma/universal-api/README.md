# <img src="https://images.mindcloud.co/apps/icons/sigma_1776371210304.png" alt="Sigma logo" width="28" height="28"> Sigma: Universal API

Sigma is a cloud analytics platform for workbooks, datasets, connections, teams, users, and audit operations.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/sigma/latest
- **Category:** Business Intelligence / Analytics & BI
- **Actions:** 30
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.sigmacomputing.com
- **Vendor API docs:** https://help.sigmacomputing.com/docs/learn-sigma

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Connections](actions/list-connections.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sigma/latest/actions/list-connections?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (30)

### Account Type

| Action | Method | Description |
| --- | --- | --- |
| [List Account Types](actions/list-account-types.md) | GET |  |

### Account Type Permission

| Action | Method | Description |
| --- | --- | --- |
| [List Account Type Permissions](actions/list-account-type-permissions.md) | GET |  |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Get Connection](actions/get-connection.md) | GET |  |

### Connection Grant

| Action | Method | Description |
| --- | --- | --- |
| [List Connection Grants](actions/list-connection-grants.md) | GET |  |

### Connection Path Grant

| Action | Method | Description |
| --- | --- | --- |
| [List Connection Path Grants](actions/list-connection-path-grants.md) | GET |  |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Get Connection Path](actions/get-connection-path.md) | GET |  |
| [List Connection Paths](actions/list-connection-paths.md) | GET |  |
| [List Connection Table Columns](actions/list-connection-table-columns.md) | GET |  |
| [List Connections](actions/list-connections.md) | GET |  |
| [Test Connection](actions/test-connection.md) | GET |  |

### Data Model

| Action | Method | Description |
| --- | --- | --- |
| [List Data Models](actions/list-data-models.md) | GET |  |

### Dataset

| Action | Method | Description |
| --- | --- | --- |
| [List Datasets](actions/list-datasets.md) | GET |  |

### Deployable Tenant

| Action | Method | Description |
| --- | --- | --- |
| [List Deployable Tenants](actions/list-deployable-tenants.md) | GET |  |

### Deployment Policy

| Action | Method | Description |
| --- | --- | --- |
| [List Deployment Policies](actions/list-deployment-policies.md) | GET |  |

### File

| Action | Method | Description |
| --- | --- | --- |
| [List Files](actions/list-files.md) | GET |  |

### Grant

| Action | Method | Description |
| --- | --- | --- |
| [List Grants](actions/list-grants.md) | GET |  |

### Member

| Action | Method | Description |
| --- | --- | --- |
| [List Members](actions/list-members.md) | GET |  |
| [List Members (Paginated)](actions/list-members-paginated.md) | GET |  |

### Organization Translation File

| Action | Method | Description |
| --- | --- | --- |
| [List Organization Translation Files](actions/list-organization-translation-files.md) | GET |  |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [List Reports](actions/list-reports.md) | GET |  |

### Saml Service Provider

| Action | Method | Description |
| --- | --- | --- |
| [List SAML Service Providers](actions/list-saml-service-providers.md) | GET |  |

### Shared Template

| Action | Method | Description |
| --- | --- | --- |
| [List Shared Templates](actions/list-shared-templates.md) | GET |  |

### Source Swap Policy

| Action | Method | Description |
| --- | --- | --- |
| [List Source Swap Policies](actions/list-source-swap-policies.md) | GET |  |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET |  |

### Team

| Action | Method | Description |
| --- | --- | --- |
| [List Teams](actions/list-teams.md) | GET |  |
| [List Teams (Paginated)](actions/list-teams-paginated.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET |  |

### Tenant

| Action | Method | Description |
| --- | --- | --- |
| [List Tenants](actions/list-tenants.md) | GET |  |

### User Attribute

| Action | Method | Description |
| --- | --- | --- |
| [List User Attributes](actions/list-user-attributes.md) | GET |  |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [List Workspaces (Paginated)](actions/list-workspaces-paginated.md) | GET |  |

