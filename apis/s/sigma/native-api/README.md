# Sigma: Native API Reference

A consolidated summary of Sigma's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://help.sigmacomputing.com/docs/learn-sigma
- **OpenAPI specification:** https://help.sigmacomputing.com/openapi/sigma-computing-public-rest-api.json
- **API base URL:** `https://aws-api.sigmacomputing.com`

## Authentication

### OAuth2

Sigma OAuth2 client-credentials authentication.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://aws-api.sigmacomputing.com/v2/auth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://help.sigmacomputing.com/docs/configure-api-credentials-and-connectors-in-sigma)

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Connection](actions/get-connection.md) | `GET /v2/connections/{connectionId}` | [docs](https://help.sigmacomputing.com/reference) |
| [Get Connection Path](actions/get-connection-path.md) | `GET /v2/connections/paths/{inodeId}` | [docs](https://help.sigmacomputing.com/reference) |
| [List Account Type Permissions](actions/list-account-type-permissions.md) | `GET /v2/accountTypes/{accountTypeId}/permissions` | [docs](https://help.sigmacomputing.com/reference) |
| [List Account Types](actions/list-account-types.md) | `GET /v2/accountTypes` | [docs](https://help.sigmacomputing.com/reference) |
| [List Connection Grants](actions/list-connection-grants.md) | `GET /v2/connections/{connectionId}/grants` | [docs](https://help.sigmacomputing.com/reference) |
| [List Connection Path Grants](actions/list-connection-path-grants.md) | `GET /v2/connections/paths/{connectionPathId}/grants` | [docs](https://help.sigmacomputing.com/reference) |
| [List Connection Paths](actions/list-connection-paths.md) | `GET /v2/connections/paths` | [docs](https://help.sigmacomputing.com/reference) |
| [List Connection Table Columns](actions/list-connection-table-columns.md) | `GET /v2/connections/tables/{tableId}/columns` | [docs](https://help.sigmacomputing.com/reference) |
| [List Connections](actions/list-connections.md) | `GET /v2/connections` | [docs](https://help.sigmacomputing.com/reference/listconnections) |
| [List Data Models](actions/list-data-models.md) | `GET /v2/dataModels` | [docs](https://help.sigmacomputing.com/reference) |
| [List Datasets](actions/list-datasets.md) | `GET /v2/datasets` | [docs](https://help.sigmacomputing.com/reference) |
| [List Deployable Tenants](actions/list-deployable-tenants.md) | `GET /v2/deploymentPolicies/tenants` | [docs](https://help.sigmacomputing.com/reference) |
| [List Deployment Policies](actions/list-deployment-policies.md) | `GET /v2/deploymentPolicies` | [docs](https://help.sigmacomputing.com/reference) |
| [List Files](actions/list-files.md) | `GET /v2/files` | [docs](https://help.sigmacomputing.com/reference) |
| [List Grants](actions/list-grants.md) | `GET /v2/grants` | [docs](https://help.sigmacomputing.com/reference) |
| [List Members](actions/list-members.md) | `GET /v2/members` | [docs](https://help.sigmacomputing.com/reference) |
| [List Members (Paginated)](actions/list-members-paginated.md) | `GET /v2.1/members` | [docs](https://help.sigmacomputing.com/reference) |
| [List Organization Translation Files](actions/list-organization-translation-files.md) | `GET /v2/translations/organization` | [docs](https://help.sigmacomputing.com/reference) |
| [List Reports](actions/list-reports.md) | `GET /v2/reports` | [docs](https://help.sigmacomputing.com/reference) |
| [List SAML Service Providers](actions/list-saml-service-providers.md) | `GET /v2/saml/service-providers` | [docs](https://help.sigmacomputing.com/reference) |
| [List Shared Templates](actions/list-shared-templates.md) | `GET /v2/shared_templates/shared_with_you` | [docs](https://help.sigmacomputing.com/reference) |
| [List Source Swap Policies](actions/list-source-swap-policies.md) | `GET /v2/sourceSwapPolicies` | [docs](https://help.sigmacomputing.com/reference) |
| [List Tags](actions/list-tags.md) | `GET /v2/tags` | [docs](https://help.sigmacomputing.com/reference) |
| [List Teams](actions/list-teams.md) | `GET /v2/teams` | [docs](https://help.sigmacomputing.com/reference) |
| [List Teams (Paginated)](actions/list-teams-paginated.md) | `GET /v2.1/teams` | [docs](https://help.sigmacomputing.com/reference) |
| [List Templates](actions/list-templates.md) | `GET /v2/templates` | [docs](https://help.sigmacomputing.com/reference) |
| [List Tenants](actions/list-tenants.md) | `GET /v2/tenants` | [docs](https://help.sigmacomputing.com/reference) |
| [List User Attributes](actions/list-user-attributes.md) | `GET /v2/user-attributes` | [docs](https://help.sigmacomputing.com/reference) |
| [List Workspaces (Paginated)](actions/list-workspaces-paginated.md) | `GET /v2.1/workspaces` | [docs](https://help.sigmacomputing.com/reference) |
| [Test Connection](actions/test-connection.md) | `GET /v2/connections/{connectionId}/test` | [docs](https://help.sigmacomputing.com/reference) |
