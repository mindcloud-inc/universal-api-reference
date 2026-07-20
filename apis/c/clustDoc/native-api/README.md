# ClustDoc: Native API Reference

A consolidated summary of ClustDoc's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://clustdoc.com/api
- **API base URL:** `https://api.clustdoc.com/api`

## Authentication

### API Token

Use a Clustdoc API token generated from Team Settings > Developers > API.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://clustdoc.com/api)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Application](actions/create-application.md) | `POST /dossiers` | [docs](https://clustdoc.com/api) |
| [Create Company](actions/create-company.md) | `POST /companies` | [docs](https://clustdoc.com/api) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://clustdoc.com/api) |
| [Create Data Field](actions/create-data-field.md) | `POST /data-fields` | [docs](https://clustdoc.com/api) |
| [Create Form](actions/create-form.md) | `POST /forms` | [docs](https://clustdoc.com/api) |
| [Create Portal](actions/create-portal.md) | `POST /portals` | [docs](https://clustdoc.com/api) |
| [Create Tag](actions/create-tag.md) | `POST /tags` | [docs](https://clustdoc.com/api) |
| [Create Template](actions/create-template.md) | `POST /templates` | [docs](https://clustdoc.com/api) |
| [List Active Contacts](actions/list-active-contacts.md) | `GET /contacts` | [docs](https://clustdoc.com/api) |
| [List Applications](actions/list-applications.md) | `GET /dossiers` | [docs](https://clustdoc.com/api) |
| [List Applications By Status](actions/list-applications-by-status.md) | `GET /dossiers` | [docs](https://clustdoc.com/api) |
| [List Applications By Template](actions/list-applications-by-template.md) | `GET /dossiers` | [docs](https://clustdoc.com/api) |
| [List Companies](actions/list-companies.md) | `GET /companies` | [docs](https://clustdoc.com/api) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://clustdoc.com/api) |
| [List Current Teams](actions/list-current-teams.md) | `GET /teams` | [docs](https://clustdoc.com/api) |
| [List Data Fields](actions/list-data-fields.md) | `GET /data-fields` | [docs](https://clustdoc.com/api) |
| [List Data Fields By Parent Type](actions/list-data-fields-by-parent-type.md) | `GET /data-fields` | [docs](https://clustdoc.com/api) |
| [List Forms](actions/list-forms.md) | `GET /forms` | [docs](https://clustdoc.com/api) |
| [List Live Templates](actions/list-live-templates.md) | `GET /templates` | [docs](https://clustdoc.com/api) |
| [List On-Time Applications](actions/list-on-time-applications.md) | `GET /dossiers` | [docs](https://clustdoc.com/api) |
| [List Owner Users](actions/list-owner-users.md) | `GET /users` | [docs](https://clustdoc.com/api) |
| [List Phone Collection Templates](actions/list-phone-collection-templates.md) | `GET /templates` | [docs](https://clustdoc.com/api) |
| [List Portals](actions/list-portals.md) | `GET /portals` | [docs](https://clustdoc.com/api) |
| [List Tags](actions/list-tags.md) | `GET /tags` | [docs](https://clustdoc.com/api) |
| [List Teams](actions/list-teams.md) | `GET /teams` | [docs](https://clustdoc.com/api) |
| [List Templates](actions/list-templates.md) | `GET /templates` | [docs](https://clustdoc.com/api) |
| [List Templates By Background](actions/list-templates-by-background.md) | `GET /templates` | [docs](https://clustdoc.com/api) |
| [List Templates By Language](actions/list-templates-by-language.md) | `GET /templates` | [docs](https://clustdoc.com/api) |
| [List Text Data Fields](actions/list-text-data-fields.md) | `GET /data-fields` | [docs](https://clustdoc.com/api) |
| [List Uploads](actions/list-uploads.md) | `GET /uploads` | [docs](https://clustdoc.com/api) |
| [List Uploads By Dossier Item](actions/list-uploads-by-dossier-item.md) | `GET /uploads` | [docs](https://clustdoc.com/api) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://clustdoc.com/api) |
| [Search Applications](actions/search-applications.md) | `GET /dossiers` | [docs](https://clustdoc.com/api) |
| [Search Companies](actions/search-companies.md) | `GET /companies` | [docs](https://clustdoc.com/api) |
| [Search Contacts](actions/search-contacts.md) | `GET /contacts` | [docs](https://clustdoc.com/api) |
| [Search Contacts By Email](actions/search-contacts-by-email.md) | `GET /contacts` | [docs](https://clustdoc.com/api) |
| [Search Forms By Title](actions/search-forms-by-title.md) | `GET /forms` | [docs](https://clustdoc.com/api) |
| [Search Portals By Title](actions/search-portals-by-title.md) | `GET /portals` | [docs](https://clustdoc.com/api) |
| [Search Tags](actions/search-tags.md) | `GET /tags` | [docs](https://clustdoc.com/api) |
| [Search Teams](actions/search-teams.md) | `GET /teams` | [docs](https://clustdoc.com/api) |
| [Search Users](actions/search-users.md) | `GET /users` | [docs](https://clustdoc.com/api) |
