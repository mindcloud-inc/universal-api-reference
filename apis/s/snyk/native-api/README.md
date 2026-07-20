# Snyk: Native API Reference

A consolidated summary of Snyk's API configuration and 60 documented operations, with links to official documentation.

- **Official docs:** https://docs.snyk.io/snyk-api/reference
- **OpenAPI specification:** https://apidocs.snyk.io/?version=2025-11-05
- **API base URL:** `https://api.snyk.io/rest`

## Authentication

### Snyk API Token

Use a Snyk personal access token. Runtime requests must send Authorization: Token <token>.

[Official authentication documentation](https://docs.snyk.io/snyk-api/authentication-for-api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/vnd.api+json` |

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 10–100). Use `starting_after` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (60 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [List Access Requests](actions/get-access-requests.md) | `GET /self/access_requests` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get API Version](actions/get-api-version.md) | `GET /openapi/:version` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get App By Client ID](actions/get-app.md) | `GET /orgs/:org_id/apps/:client_id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List App Bots](actions/get-app-bots.md) | `GET /orgs/:org_id/app_bots` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get App By ID](actions/get-app-by-id.md) | `GET /orgs/:org_id/apps/creations/:app_id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Group App Installs](actions/get-app-installs-for-group.md) | `GET /groups/:group_id/apps/installs` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Organization App Installs](actions/get-app-installs-for-org.md) | `GET /orgs/:org_id/apps/installs` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List User App Installs](actions/get-app-installs-for-user.md) | `GET /self/apps/installs` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Organization Apps](actions/get-apps.md) | `GET /orgs/:org_id/apps` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Asset](actions/get-asset.md) | `GET /groups/:group_id/assets/:asset_id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Collection](actions/get-collection.md) | `GET /orgs/:org_id/collections/:collection_id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Collections](actions/get-collections.md) | `GET /orgs/:org_id/collections` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Custom Base Image](actions/get-custom-base-image.md) | `GET /custom_base_images/:custombaseimage_id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Custom Base Images](actions/get-custom-base-images.md) | `GET /custom_base_images` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Group Asset Filter Fields](actions/get-filter-fields-group.md) | `GET /groups/:group_id/inventory/assets/filters` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Group Asset Filter Values](actions/get-filter-values-group.md) | `GET /groups/:group_id/inventory/assets/filters/:filter_id/values` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Group](actions/get-group.md) | `GET /groups/:group_id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Group Export](actions/get-group-export.md) | `GET /groups/:group_id/export/:export_id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Group Asset Group Fields](actions/get-group-fields-group.md) | `GET /groups/:group_id/inventory/assets/groups` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Group Issue](actions/get-group-issue-by-issue-id.md) | `GET /groups/:group_id/issues/:issue_id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Package Issues](actions/get-issues-per-purl.md) | `GET /orgs/:org_id/packages/:purl/issues` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Group Service Accounts](actions/get-many-group-service-account.md) | `GET /groups/:group_id/service_accounts` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Organization Service Accounts](actions/get-many-org-service-accounts.md) | `GET /orgs/:org_id/service_accounts` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Group Service Account](actions/get-one-group-service-account.md) | `GET /groups/:group_id/service_accounts/:serviceaccount_id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Organization Service Account](actions/get-one-org-service-account.md) | `GET /orgs/:org_id/service_accounts/:serviceaccount_id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Organization](actions/get-org.md) | `GET /orgs/:org_id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Organization App Creations](actions/get-org-apps.md) | `GET /orgs/:org_id/apps/creations` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Organization Issue](actions/get-org-issue-by-issue-id.md) | `GET /orgs/:org_id/issues/:issue_id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Organization Policies](actions/get-org-policies.md) | `GET /orgs/:org_id/policies` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Organization Policy](actions/get-org-policy.md) | `GET /orgs/:org_id/policies/:policy_id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Organization Policy Events](actions/get-org-policy-events.md) | `GET /orgs/:org_id/policies/:policy_id/events` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Organization Project](actions/get-org-project.md) | `GET /orgs/:org_id/projects/:project_id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Target](actions/get-orgs-target.md) | `GET /orgs/:org_id/targets/:target_id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Targets](actions/get-orgs-targets.md) | `GET /orgs/:org_id/targets` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Collection Projects](actions/get-projects-of-collection.md) | `GET /orgs/:org_id/collections/:collection_id/relationships/projects` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Self](actions/get-self.md) | `GET /self` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get Tenant](actions/get-tenant.md) | `GET /tenants/:tenant_id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Tenant Memberships](actions/get-tenant-memberships.md) | `GET /tenants/:tenant_id/memberships` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [Get User](actions/get-user.md) | `GET /orgs/:org_id/users/:id` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List User App Sessions](actions/get-user-app-sessions.md) | `GET /self/apps/:app_id/sessions` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List User Installed Apps](actions/get-user-installed-apps.md) | `GET /self/apps` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List API Versions](actions/list-api-versions.md) | `GET /openapi` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Asset Projects](actions/list-asset-projects.md) | `GET /groups/:group_id/assets/:asset_id/relationships/projects` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Group Inventory Assets](actions/list-assets-group.md) | `GET /groups/:group_id/inventory/assets` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Group Audit Logs](actions/list-group-audit-logs.md) | `GET /groups/:group_id/audit_logs/search` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Group Issues](actions/list-group-issues.md) | `GET /groups/:group_id/issues` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Group Memberships](actions/list-group-memberships.md) | `GET /groups/:group_id/memberships` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Group Policies](actions/list-group-policies.md) | `GET /groups/:group_id/policies` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Group SSO Connection Users](actions/list-group-sso-connection-users.md) | `GET /groups/:group_id/sso_connections/:sso_id/users` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Group SSO Connections](actions/list-group-sso-connections.md) | `GET /groups/:group_id/sso_connections` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Group Organization Memberships](actions/list-group-user-org-memberships.md) | `GET /groups/:group_id/org_memberships` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Organization Issues](actions/list-org-issues.md) | `GET /orgs/:org_id/issues` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Organization Memberships](actions/list-org-memberships.md) | `GET /orgs/:org_id/memberships` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Organization Projects](actions/list-org-projects.md) | `GET /orgs/:org_id/projects` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Organizations](actions/list-orgs.md) | `GET /orgs` | [docs](https://docs.snyk.io/snyk-api/reference/orgs) |
| [List Organizations In Group](actions/list-orgs-in-group.md) | `GET /groups/:group_id/orgs` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Personal Access Tokens](actions/list-personal-access-token.md) | `GET /self/personal_access_tokens` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Related Assets](actions/list-related-assets.md) | `GET /groups/:group_id/assets/:asset_id/relationships/assets` | [docs](https://docs.snyk.io/snyk-api/reference) |
| [List Tenants](actions/list-tenants.md) | `GET /tenants` | [docs](https://docs.snyk.io/snyk-api/reference) |
