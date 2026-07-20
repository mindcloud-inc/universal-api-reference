# DotCMS: Native API Reference

A consolidated summary of DotCMS's API configuration and 31 documented operations, with links to official documentation.

- **Official docs:** https://dev.dotcms.com/docs/rest-apis
- **OpenAPI specification:** https://demo.dotcms.com/api/openapi.json
- **API base URL:** `https://demo.dotcms.com/`

## Authentication

### API Token

Use a DotCMS API token. MindCloud sends it as a bearer token in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://www.dotcms.com/docs/latest/rest-api-authentication)

## Endpoints (31 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Export Categories](actions/export-categories.md) | `GET /api/v1/categories/_export` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [Filter Users](actions/filter-users.md) | `GET /api/v1/users/filter` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [Get App Configuration](actions/get-app-configuration.md) | `GET /api/v1/appconfiguration` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [Get Content Type Base Types](actions/get-content-type-base-types.md) | `GET /api/v1/contenttype/basetypes` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [Get Current Site](actions/get-current-site.md) | `GET /api/v1/site/currentSite` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [Get Current User](actions/get-current-user.md) | `GET /api/v1/users/current` | [docs](https://dev.dotcms.com/docs/rest-api-authentication) |
| [Get Default Site](actions/get-default-site.md) | `GET /api/v1/site/defaultSite` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [Get Health](actions/get-health.md) | `GET /api/v1/health` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [Get Health Liveness](actions/get-health-liveness.md) | `GET /api/v1/health/liveness` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [Get Health Readiness](actions/get-health-readiness.md) | `GET /api/v1/health/readiness` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [Get Health Status](actions/get-health-status.md) | `GET /api/v1/health/status` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [Get Login As Data](actions/get-login-as-data.md) | `GET /api/v1/users/loginAsData` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [Get Menus](actions/get-menus.md) | `GET /api/v1/menu` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Apps](actions/list-apps.md) | `GET /api/v1/apps` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Categories](actions/list-categories.md) | `GET /api/v1/categories` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Content Types](actions/list-content-types.md) | `GET /api/v1/contenttype` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Field Types](actions/list-field-types.md) | `GET /api/v1/fieldTypes` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Languages](actions/list-languages.md) | `GET /api/v1/languages` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Languages V2](actions/list-languages-v2.md) | `GET /api/v2/languages` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Page Types](actions/list-page-types.md) | `GET /api/v1/page/types` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Permissions](actions/list-permissions.md) | `GET /api/v1/permissions` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Relationship Cardinalities](actions/list-relationship-cardinalities.md) | `GET /api/v1/relationships/cardinalities` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Role Layouts](actions/list-role-layouts.md) | `GET /api/v1/roles/layouts` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Roles](actions/list-roles.md) | `GET /api/v1/roles` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Site Thumbnails](actions/list-site-thumbnails.md) | `GET /api/v1/site/thumbnails` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Sites](actions/list-sites.md) | `GET /api/v1/site` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Tags](actions/list-tags.md) | `GET /api/v2/tags` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Templates](actions/list-templates.md) | `GET /api/v1/templates` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Workflow Actionlets](actions/list-workflow-actionlets.md) | `GET /api/v1/workflow/actionlets` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [List Workflow Schemes](actions/list-workflow-schemes.md) | `GET /api/v1/workflow/schemes` | [docs](https://dev.dotcms.com/docs/api-playground) |
| [Search Roles](actions/search-roles.md) | `GET /api/v1/roles/_search` | [docs](https://dev.dotcms.com/docs/api-playground) |
