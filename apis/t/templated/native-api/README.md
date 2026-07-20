# Templated: Native API Reference

A consolidated summary of Templated's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://templated.io/docs/
- **API base URL:** `https://api.templated.io`

## Authentication

### API Key

Use a Templated API key in the Authorization bearer header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://templated.io/docs/authentication/)

## API conventions

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 25). Use `page` in the query string to choose the page; numbering starts at 0.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Clone Template](actions/clone-template.md) | `POST /v1/template/:id/clone` | [docs](https://templated.io/docs/templates/clone/) |
| [Create Folder](actions/create-folder.md) | `POST /v1/folder` | [docs](https://templated.io/docs/folders/create/) |
| [Create Render](actions/create-render.md) | `POST /v1/render` | [docs](https://templated.io/docs/renders/create/) |
| [Create Template](actions/create-template.md) | `POST /v1/template` | [docs](https://templated.io/docs/templates/create/) |
| [Delete Folder](actions/delete-folder.md) | `DELETE /v1/folder/:id` | [docs](https://templated.io/docs/folders/delete/) |
| [Delete Render](actions/delete-render.md) | `DELETE /v1/render/:id` | [docs](https://templated.io/docs/renders/delete/) |
| [Delete Template](actions/delete-template.md) | `DELETE /v1/template/:id` | [docs](https://templated.io/docs/templates/delete/) |
| [Duplicate Render](actions/duplicate-render.md) | `POST /v1/render/:id/duplicate` | [docs](https://templated.io/docs/renders/duplicate/) |
| [Duplicate Template](actions/duplicate-template.md) | `POST /v1/template/:id/duplicate` | [docs](https://templated.io/docs/templates/duplicate/) |
| [Get Account Information](actions/get-account-information.md) | `GET /v1/account` | [docs](https://templated.io/docs/account/) |
| [List Folder Templates](actions/list-folder-templates.md) | `GET /v1/folder/:id/templates` | [docs](https://templated.io/docs/folders/templates/) |
| [List Folders](actions/list-folders.md) | `GET /v1/folders` | [docs](https://templated.io/docs/folders/list/) |
| [List Gallery Templates](actions/list-gallery-templates.md) | `GET /v1/templates/gallery` | [docs](https://templated.io/docs/templates/gallery/) |
| [List Renders](actions/list-renders.md) | `GET /v1/renders` | [docs](https://templated.io/docs/renders/list/) |
| [List Template Layers](actions/list-template-layers.md) | `GET /v1/template/:id/layers` | [docs](https://templated.io/docs/templates/layers/) |
| [List Template Pages](actions/list-template-pages.md) | `GET /v1/template/:id/pages` | [docs](https://templated.io/docs/templates/pages/) |
| [List Template Renders](actions/list-template-renders.md) | `GET /v1/template/:id/renders` | [docs](https://templated.io/docs/templates/renders/) |
| [List Templates](actions/list-templates.md) | `GET /v1/templates` | [docs](https://templated.io/docs/templates/list/) |
| [Merge Renders](actions/merge-renders.md) | `POST /v1/render/merge` | [docs](https://templated.io/docs/renders/merge/) |
| [Move Template to Folder](actions/move-template-to-folder.md) | `PUT /v1/folder/:folderId/template/:templateId` | [docs](https://templated.io/docs/folders/template/) |
| [Retrieve Render](actions/retrieve-render.md) | `GET /v1/render/:id` | [docs](https://templated.io/docs/renders/retrieve/) |
| [Retrieve Template](actions/retrieve-template.md) | `GET /v1/template/:id` | [docs](https://templated.io/docs/templates/retrieve/) |
| [Update Folder](actions/update-folder.md) | `PUT /v1/folder/:id` | [docs](https://templated.io/docs/folders/update/) |
| [Update Template](actions/update-template.md) | `PUT /v1/template/:id` | [docs](https://templated.io/docs/templates/update/) |
