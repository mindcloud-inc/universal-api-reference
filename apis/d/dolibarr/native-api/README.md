# Dolibarr: Native API Reference

A consolidated summary of Dolibarr's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)
- **OpenAPI specification:** https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php/explorer/swagger.json
- **API base URL:** `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`

## Authentication

### API Key

Authenticate to Dolibarr REST API using the API key generated on a Dolibarr user record.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
DOLAPIKEY: <apiKey>
```

[Official authentication documentation](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer))

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `page` in the query string to choose the page; numbering starts at 0.

## Filtering

Send filters in the query string. Supported operators: `contains`, `eq`.

## Sorting

Set the sort field with `sortfield` in the query string. Set the direction separately with `sortorder`. Use `ASC` for ascending order and `DESC` for descending order. Only one sort field is accepted.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Agenda Event](actions/get-agenda-event.md) | `GET /agendaevents/{id}` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [Get Category](actions/get-category.md) | `GET /categories/{id}` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [Get Company Setup](actions/get-company-setup.md) | `GET /setup/company` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [Get Country](actions/get-country.md) | `GET /setup/dictionary/countries/{id}` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [Get Country By Code](actions/get-country-by-code.md) | `GET /setup/dictionary/countries/byCode/{code}` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [Get Country By ISO](actions/get-country-by-iso.md) | `GET /setup/dictionary/countries/byISO/{iso}` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [Get Current User Info](actions/get-current-user-info.md) | `GET /users/info` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [Get Email Template](actions/get-email-template.md) | `GET /emailtemplates/{id}` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [Get Email Template By Label](actions/get-email-template-by-label.md) | `GET /emailtemplates/label/{label}` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [Get Object Link](actions/get-object-link.md) | `GET /objectlinks/{id}` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [Get State](actions/get-state.md) | `GET /setup/dictionary/states/{id}` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [Get Status](actions/get-status.md) | `GET /status` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [Get User](actions/get-user.md) | `GET /users/{id}` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [Get User By Email](actions/get-user-by-email.md) | `GET /users/email/{email}` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [Get User By Login](actions/get-user-by-login.md) | `GET /users/login/{login}` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [Get User Group](actions/get-user-group.md) | `GET /users/groups/{group}` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [List Action Triggers](actions/list-action-triggers.md) | `GET /setup/actiontriggers` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [List Agenda Events](actions/list-agenda-events.md) | `GET /agendaevents` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [List Categories](actions/list-categories.md) | `GET /categories` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [List Category Objects](actions/list-category-objects.md) | `GET /categories/{id}/objects` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [List Countries](actions/list-countries.md) | `GET /setup/dictionary/countries` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [List Currencies](actions/list-currencies.md) | `GET /setup/dictionary/currencies` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [List Current User Groups](actions/list-current-user-groups.md) | `GET /users/groups` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [List Documents](actions/list-documents.md) | `GET /documents` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [List Email Templates](actions/list-email-templates.md) | `GET /emailtemplates` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [List Enabled Modules](actions/list-enabled-modules.md) | `GET /setup/modules` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [List Object Categories](actions/list-object-categories.md) | `GET /categories/object/{type}/{id}` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [List Object Links](actions/list-object-links.md) | `GET /objectlinks` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [List States](actions/list-states.md) | `GET /setup/dictionary/states` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://wiki.dolibarr.org/index.php/Module_Web_Services_API_REST_(developer)) |
