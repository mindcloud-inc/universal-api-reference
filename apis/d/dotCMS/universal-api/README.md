# <img src="https://images.mindcloud.co/apps/icons/dotcms-square-icon_1775485047065.png" alt="DotCMS logo" width="28" height="28"> DotCMS: Universal API

DotCMS is a hybrid CMS and digital experience platform for managing content, pages, sites, workflows, users, templates, and related administrative resources through a large REST API surface.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dotCMS/latest
- **Category:** Website & App Building / CMS
- **Actions:** 31
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dotcms.com/
- **Vendor API docs:** https://dev.dotcms.com/docs/rest-apis

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Current User](actions/get-current-user.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (31)

### Categories

| Action | Method | Description |
| --- | --- | --- |
| [Export Categories](actions/export-categories.md) | GET | Retrieves category records as a CSV export from DotCMS. |
| [List Categories](actions/list-categories.md) | GET | Retrieves category records available in DotCMS. |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Get App Configuration](actions/get-app-configuration.md) | GET | Retrieves app configuration settings from DotCMS. |
| [Get Content Type Base Types](actions/get-content-type-base-types.md) | GET | Retrieves base content type definitions from DotCMS. |
| [Get Current Site](actions/get-current-site.md) | GET | Retrieves the current site from DotCMS. |
| [Get Default Site](actions/get-default-site.md) | GET | Retrieves the default site from DotCMS. |
| [Get Health](actions/get-health.md) | GET | Retrieves overall health status from DotCMS. |
| [Get Health Liveness](actions/get-health-liveness.md) | GET | Retrieves liveness health status from DotCMS. |
| [Get Health Readiness](actions/get-health-readiness.md) | GET | Retrieves readiness health status from DotCMS. |
| [Get Health Status](actions/get-health-status.md) | GET | Retrieves system health flags from DotCMS. |
| [List Apps](actions/list-apps.md) | GET | Finds available apps in DotCMS by filter. |
| [List Content Types](actions/list-content-types.md) | GET | Retrieves content type records from DotCMS. |
| [List Field Types](actions/list-field-types.md) | GET | Retrieves available field types from DotCMS. |
| [List Languages](actions/list-languages.md) | GET | Retrieves configured language records from DotCMS. |
| [List Languages V2](actions/list-languages-v2.md) | GET | Retrieves languages for content in DotCMS. |
| [List Relationship Cardinalities](actions/list-relationship-cardinalities.md) | GET | Retrieves relationship cardinality options from DotCMS. |
| [List Site Thumbnails](actions/list-site-thumbnails.md) | GET | Retrieves site thumbnail data from DotCMS. |
| [List Sites](actions/list-sites.md) | GET | Retrieves accessible site records from DotCMS. |

### Pages

| Action | Method | Description |
| --- | --- | --- |
| [Get Menus](actions/get-menus.md) | GET | Retrieves available navigation menus from DotCMS. |
| [List Page Types](actions/list-page-types.md) | GET | Retrieves page content type records from DotCMS. |

### Permissions

| Action | Method | Description |
| --- | --- | --- |
| [List Permissions](actions/list-permissions.md) | GET | Retrieves permission metadata definitions from DotCMS. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [List Role Layouts](actions/list-role-layouts.md) | GET | Retrieves role layout records from DotCMS. |
| [List Roles](actions/list-roles.md) | GET | Retrieves root role records from DotCMS. |
| [Search Roles](actions/search-roles.md) | GET | Finds roles in DotCMS by name, key, or ID. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [List Tags](actions/list-tags.md) | GET | Finds tags in DotCMS by search criteria. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [List Templates](actions/list-templates.md) | GET | Retrieves available template records from DotCMS. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Filter Users](actions/filter-users.md) | GET | Finds users in DotCMS by filter criteria. |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the authenticated user from DotCMS. |
| [Get Login As Data](actions/get-login-as-data.md) | GET | Retrieves impersonation candidate users from DotCMS. |

### Workflows

| Action | Method | Description |
| --- | --- | --- |
| [List Workflow Actionlets](actions/list-workflow-actionlets.md) | GET | Retrieves available workflow actionlets from DotCMS. |
| [List Workflow Schemes](actions/list-workflow-schemes.md) | GET | Retrieves workflow scheme records from DotCMS. |

