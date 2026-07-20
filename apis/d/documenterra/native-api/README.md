# Documenterra: Native API Reference

A consolidated summary of Documenterra's API configuration and 19 documented operations, with links to official documentation.

- **Official docs:** https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-dokumenterry
- **API base URL:** `https://mindclouddocumenterra.try.documenterra.net/api/v1`

## Authentication

### Basic Auth (Login + API Key)

Authenticate to a tenant-scoped Documenterra portal with your account login as the Basic-auth username and your API key as the Basic-auth password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://docs.documenterra.ru/articles/manual/api-dokumenterry/)

## API conventions

Responses from this API use JSON.

## Endpoints (19 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Page](actions/create-page.md) | `POST /projects/:projectId/articles` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-sozdaniye-stranitsy) |
| [Create Tree Folder](actions/create-tree-folder.md) | `POST /projects/:projectId/toc/nodes` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-sozdaniye-elementa-dereva-stranits-papki) |
| [Delete Multiple Pages](actions/delete-multiple-pages.md) | `DELETE /projects/:id/articles` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-udaleniye-neskolkikh-stranits) |
| [Delete Page](actions/delete-page.md) | `DELETE /projects/:id/articles/:topicId` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-udaleniye-stranitsy) |
| [Delete Tree Element](actions/delete-tree-element.md) | `DELETE /projects/:projectId/toc/nodes/:tocNodeId` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-udaleniye-elementa-dereva-stranits) |
| [Get Multiple Tree Elements](actions/get-multiple-tree-elements.md) | `GET /projects/:projectId/toc/nodes` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-polucheniye-neskolkikh-elementov-dereva-stranits) |
| [Get Page](actions/get-page.md) | `GET /projects/:id/articles/:topicId` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-polucheniye-stranitsy) |
| [Get Page Views](actions/get-page-views.md) | `GET /reports/user-events/:prLogin/articles` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-polucheniye-prosmotrov-stranitsy) |
| [Get Project](actions/get-project.md) | `GET /projects/:id` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-polucheniye-informatsii-o-proyekte-publikatsii) |
| [Get Search Queries](actions/get-search-queries.md) | `GET /reports/user-events/:prLogin/search-queries` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-polucheniye-poiskovykh-zaprosov) |
| [Get Tree Element](actions/get-tree-element.md) | `GET /projects/:projectId/toc/nodes/:nodeId` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-polucheniye-elementa-dereva-stranits) |
| [List Child Tree Elements](actions/list-child-tree-elements.md) | `GET /projects/:projectId/toc/nodes/:tocNodeId/children` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-polucheniye-dochernikh-elementov-dereva-stranits) |
| [List Pages](actions/list-pages.md) | `GET /projects/:id/articles` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-polucheniye-vsekh-stranits-proyekta-publikatsii) |
| [List Project Access Users](actions/list-project-access-users.md) | `GET /projects/:id/users` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-poluchenie-spiska-polzovateley-s-dostupom-k-proektu-publikatsii) |
| [List Projects](actions/list-projects.md) | `GET /projects` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-polucheniye-vsekh-proyektov-i-publikatsiy) |
| [List User Profiles](actions/list-user-profiles.md) | `GET /users` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-poluchenie-profiley-polzovateley) |
| [Search Portal](actions/search-portal.md) | `GET /search` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-poisk-po-portalu) |
| [Update Page](actions/update-page.md) | `PATCH /projects/:projectId/articles/:topicId` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-obnovleniye-stranitsy) |
| [Update Tree Element](actions/update-tree-element.md) | `PATCH /projects/:projectId/toc/nodes/:tocNodeId` | [docs](https://docs.documenterra.ru/articles/rukovodstvo-polzovatelya-dokumenterry/api-obnovleniye-elementa-dereva-stranits) |
