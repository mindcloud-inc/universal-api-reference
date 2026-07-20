# GitBook: Native API Reference

A consolidated summary of GitBook's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://gitbook.com/docs/developers/gitbook-api/api-reference
- **OpenAPI specification:** https://api.gitbook.com/openapi.yaml
- **API base URL:** `https://api.gitbook.com/v1`

## Authentication

### Personal Access Token

Authenticate with a GitBook personal access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://gitbook.com/docs/developers/gitbook-api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string as the pagination cursor.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Space To Site](actions/add-space-to-site.md) | `POST /orgs/:organizationId/sites/:siteId/site-spaces` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/docs-sites) |
| [Create Change Request](actions/create-change-request.md) | `POST /spaces/:spaceId/change-requests` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/change-requests) |
| [Create Collection](actions/create-collection.md) | `POST /orgs/:organizationId/collections` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/collections) |
| [Create Site](actions/create-site.md) | `POST /orgs/:organizationId/sites` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/docs-sites) |
| [Create Space](actions/create-space.md) | `POST /orgs/:organizationId/spaces` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/spaces) |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /user` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/users) |
| [Get Collection](actions/get-collection.md) | `GET /collections/:collectionId` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/collections) |
| [Get Organization](actions/get-organization.md) | `GET /orgs/:organizationId` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/organizations) |
| [Get Site](actions/get-site.md) | `GET /orgs/:organizationId/sites/:siteId` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/docs-sites) |
| [Get Space](actions/get-space.md) | `GET /spaces/:spaceId` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/spaces) |
| [Get Space Page](actions/get-space-page.md) | `GET /spaces/:spaceId/content/page/:pageId` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/spaces) |
| [List Change Requests](actions/list-change-requests.md) | `GET /spaces/:spaceId/change-requests` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/change-requests) |
| [List Collections](actions/list-collections.md) | `GET /orgs/:organizationId/collections` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/collections) |
| [List Organization Members](actions/list-organization-members.md) | `GET /orgs/:organizationId/members` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/organizations) |
| [List Organizations](actions/list-organizations.md) | `GET /orgs` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/organizations) |
| [List Site Spaces](actions/list-site-spaces.md) | `GET /orgs/:organizationId/sites/:siteId/site-spaces` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/docs-sites) |
| [List Sites](actions/list-sites.md) | `GET /orgs/:organizationId/sites` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/docs-sites) |
| [List Space Files](actions/list-space-files.md) | `GET /spaces/:spaceId/content/files` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/spaces) |
| [List Space Pages](actions/list-space-pages.md) | `GET /spaces/:spaceId/content/pages` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/spaces) |
| [List Spaces](actions/list-spaces.md) | `GET /orgs/:organizationId/spaces` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/spaces) |
| [Search Site](actions/search-site.md) | `POST /orgs/:organizationId/sites/:siteId/search` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/docs-sites) |
| [Update Collection](actions/update-collection.md) | `PATCH /collections/:collectionId` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/collections) |
| [Update Site](actions/update-site.md) | `PATCH /orgs/:organizationId/sites/:siteId` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/docs-sites) |
| [Update Space](actions/update-space.md) | `PATCH /spaces/:spaceId` | [docs](https://gitbook.com/docs/developers/gitbook-api/api-reference/spaces) |
