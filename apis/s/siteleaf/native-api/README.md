# Siteleaf: Native API Reference

A consolidated summary of Siteleaf's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://learn.siteleaf.com/api/
- **API base URL:** `https://api.siteleaf.com/v2`

## Authentication

### API Key + API Secret

Use your Siteleaf account API key as the username and your API secret as the password.

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

[Official authentication documentation](https://learn.siteleaf.com/api/authentication/)

## Pagination

Use `per_page` in the query string to set the page size (default 30). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | `POST /sites/:site_id/collections` | [docs](https://learn.siteleaf.com/api/collections/#create-a-collection) |
| [Create Document](actions/create-document.md) | `POST /sites/:site_id/collections/:path/documents` | [docs](https://learn.siteleaf.com/api/documents/#create-a-document) |
| [Create or Replace File](actions/create-or-replace-file.md) | `PUT /sites/:site_id/source/:name` | [docs](https://learn.siteleaf.com/api/source/#create-or-replace-a-file) |
| [Create Page](actions/create-page.md) | `POST /sites/:site_id/pages` | [docs](https://learn.siteleaf.com/api/pages/#create-a-page) |
| [Create Site](actions/create-site.md) | `POST /sites` | [docs](https://learn.siteleaf.com/api/sites/#create-a-site) |
| [Delete Collection](actions/delete-collection.md) | `DELETE /sites/:site_id/collections/:path` | [docs](https://learn.siteleaf.com/api/collections/#delete-a-collection) |
| [Delete Document](actions/delete-document.md) | `DELETE /documents/:document_id` | [docs](https://learn.siteleaf.com/api/documents/#delete-a-document) |
| [Delete File](actions/delete-file.md) | `DELETE /sites/:site_id/source/:name` | [docs](https://learn.siteleaf.com/api/source/#delete-a-file) |
| [Delete Page](actions/delete-page.md) | `DELETE /pages/:page_id` | [docs](https://learn.siteleaf.com/api/pages/#delete-a-page) |
| [Delete Site](actions/delete-site.md) | `DELETE /sites/:site_id` | [docs](https://learn.siteleaf.com/api/sites/#delete-a-site) |
| [Get Authenticated User](actions/get-authenticated-user.md) | `GET /users/me` | [docs](https://learn.siteleaf.com/api/users/#current-user) |
| [Get Collection](actions/get-collection.md) | `GET /sites/:site_id/collections/:path` | [docs](https://learn.siteleaf.com/api/collections/#get-a-collection) |
| [Get Document](actions/get-document.md) | `GET /documents/:document_id` | [docs](https://learn.siteleaf.com/api/documents/#get-a-document) |
| [Get Files](actions/get-files.md) | `GET /sites/:site_id/source/:name` | [docs](https://learn.siteleaf.com/api/source/#get-files) |
| [Get Page](actions/get-page.md) | `GET /pages/:page_id` | [docs](https://learn.siteleaf.com/api/pages/#get-a-page) |
| [Get Site](actions/get-site.md) | `GET /sites/:site_id` | [docs](https://learn.siteleaf.com/api/sites/#get-a-site) |
| [List Collection Files](actions/list-collection-files.md) | `GET /sites/:site_id/collections/:path/files` | [docs](https://learn.siteleaf.com/api/collections/#list-collection-files) |
| [List Collections](actions/list-collections.md) | `GET /sites/:site_id/collections` | [docs](https://learn.siteleaf.com/api/collections/#list-collections) |
| [List Documents](actions/list-documents.md) | `GET /sites/:site_id/collections/:path/documents` | [docs](https://learn.siteleaf.com/api/documents/#list-documents) |
| [List Pages](actions/list-pages.md) | `GET /sites/:site_id/pages` | [docs](https://learn.siteleaf.com/api/pages/#list-pages) |
| [List Post Categories](actions/list-post-categories.md) | `GET /sites/:site_id/categories` | [docs](https://learn.siteleaf.com/api/sites/#list-post-categories) |
| [List Post Tags](actions/list-post-tags.md) | `GET /sites/:site_id/tags` | [docs](https://learn.siteleaf.com/api/sites/#list-post-tags) |
| [List Sites](actions/list-sites.md) | `GET /sites` | [docs](https://learn.siteleaf.com/api/sites/#list-your-sites) |
| [List Users](actions/list-users.md) | `GET /sites/:site_id/users` | [docs](https://learn.siteleaf.com/api/users/#list-users) |
| [Listen to Job](actions/listen-to-job.md) | `GET /jobs/:job_id` | [docs](https://learn.siteleaf.com/api/jobs/#listen-to-a-job) |
| [Publish Site](actions/publish-site.md) | `POST /sites/:site_id/publish` | [docs](https://learn.siteleaf.com/api/sites/#publish-a-site) |
| [Update Collection](actions/update-collection.md) | `PUT /sites/:site_id/collections/:path` | [docs](https://learn.siteleaf.com/api/collections/#update-a-collection) |
| [Update Document](actions/update-document.md) | `PUT /documents/:document_id` | [docs](https://learn.siteleaf.com/api/documents/#update-a-document) |
| [Update Page](actions/update-page.md) | `PUT /pages/:page_id` | [docs](https://learn.siteleaf.com/api/pages/#update-a-page) |
| [Update Site](actions/update-site.md) | `PUT /sites/:site_id` | [docs](https://learn.siteleaf.com/api/sites/#update-a-site) |
