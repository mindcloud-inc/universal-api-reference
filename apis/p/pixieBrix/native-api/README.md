# PixieBrix: Native API Reference

A consolidated summary of PixieBrix's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://docs.pixiebrix.com/developer-api/making-an-api-request
- **OpenAPI specification:** https://app.pixiebrix.com/api/openapi/
- **API base URL:** `https://app.pixiebrix.com`

## Authentication

### Service Account Token

Authenticate to the PixieBrix Developer API with a PixieBrix service account token.

### Credentials

- **Service Account Token:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.pixiebrix.com/developer-api/service-accounts)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json; version=2.0` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 100; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 1.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Database Record](actions/create-database-record.md) | `POST /api/databases/:database_pk/records/` | [docs](https://docs.pixiebrix.com/developer-api/database-apis) |
| [Get Current User](actions/get-current-user.md) | `GET /api/me/` | [docs](https://app.pixiebrix.com/api/docs/) |
| [Get Database](actions/get-database.md) | `GET /api/organizations/:organization_pk/databases/:id/` | [docs](https://docs.pixiebrix.com/developer-api/database-apis) |
| [Get Database Asset](actions/get-database-asset.md) | `GET /api/databases/:database_pk/assets/:id/` | [docs](https://docs.pixiebrix.com/developer-api/database-apis) |
| [Get Database Record](actions/get-database-record.md) | `GET /api/databases/:database_pk/records/:key/` | [docs](https://docs.pixiebrix.com/developer-api/database-apis) |
| [Get Deployment](actions/get-deployment.md) | `GET /api/deployments/:id/` | [docs](https://docs.pixiebrix.com/developer-api/deployment-apis) |
| [Get Group](actions/get-group.md) | `GET /api/groups/:id/` | [docs](https://app.pixiebrix.com/api/docs/) |
| [Get Organization](actions/get-organization.md) | `GET /api/organizations/:organization_pk/` | [docs](https://app.pixiebrix.com/api/docs/) |
| [Get Organization Member](actions/get-organization-member.md) | `GET /api/organizations/:organization_pk/members/:id/` | [docs](https://app.pixiebrix.com/api/docs/) |
| [Get Package](actions/get-package.md) | `GET /api/bricks/:id/` | [docs](https://docs.pixiebrix.com/developer-api/package-management-apis) |
| [Get Registry Brick](actions/get-registry-brick.md) | `GET /api/registry/bricks/:name/` | [docs](https://docs.pixiebrix.com/developer-api/package-management-apis) |
| [Health Check](actions/health-check.md) | `GET /api/health/` | [docs](https://docs.pixiebrix.com/developer-api/health-check-apis) |
| [List Database Assets](actions/list-database-assets.md) | `GET /api/databases/:database_pk/assets/` | [docs](https://docs.pixiebrix.com/developer-api/database-apis) |
| [List Database Records](actions/list-database-records.md) | `GET /api/databases/:database_pk/records/` | [docs](https://docs.pixiebrix.com/developer-api/database-apis) |
| [List Databases](actions/list-databases.md) | `GET /api/organizations/:organization_pk/databases/` | [docs](https://docs.pixiebrix.com/developer-api/database-apis) |
| [List Deployment Errors](actions/list-deployment-errors.md) | `GET /api/deployments/:deployment_pk/errors/` | [docs](https://app.pixiebrix.com/api/docs/) |
| [List Deployments](actions/list-deployments.md) | `GET /api/organizations/:organization_pk/deployments/` | [docs](https://docs.pixiebrix.com/developer-api/deployment-apis) |
| [List Groups](actions/list-groups.md) | `GET /api/organizations/:organization_pk/groups/` | [docs](https://app.pixiebrix.com/api/docs/) |
| [List Organization Memberships](actions/list-organization-memberships.md) | `GET /api/organizations/:organization_pk/memberships/` | [docs](https://app.pixiebrix.com/api/docs/) |
| [List Organizations](actions/list-organizations.md) | `GET /api/organizations/` | [docs](https://app.pixiebrix.com/api/docs/) |
| [List Package Versions](actions/list-package-versions.md) | `GET /api/bricks/:id/versions/` | [docs](https://docs.pixiebrix.com/developer-api/package-management-apis) |
| [List Packages](actions/list-packages.md) | `GET /api/organizations/:organization_pk/bricks/` | [docs](https://docs.pixiebrix.com/developer-api/package-management-apis) |
| [List Registry Bricks](actions/list-registry-bricks.md) | `GET /api/registry/bricks/` | [docs](https://docs.pixiebrix.com/developer-api/package-management-apis) |
| [Update Database Record](actions/update-database-record.md) | `PUT /api/databases/:database_pk/records/` | [docs](https://docs.pixiebrix.com/developer-api/database-apis) |
