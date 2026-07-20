# Webflow: Native API Reference

A consolidated summary of Webflow's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://developers.webflow.com/data/reference
- **API base URL:** `https://api.webflow.com/v2`

## Authentication

### OAuth 2.0

Connect Webflow using OAuth 2.0 authorization code flow.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://webflow.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.webflow.com/oauth/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `app_subscriptions:read assets:read assets:write authorized_user:read cms:read cms:write comments:read comments:write components:read components:write custom_code:read custom_code:write ecommerce:read ecommerce:write forms:read forms:write pages:read pages:write site_activity:read site_config:read site_config:write sites:read sites:write users:read users:write workspace:read workspace:write`.

[Official authentication documentation](https://developers.webflow.com/data/reference/oauth-apps/authorized-by-users)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `sites`.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–100). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Collection](actions/create-collection.md) | `POST /sites/:site_id/collections` | [docs](https://developers.webflow.com/data/reference/cms/collections/create) |
| [Create Items](actions/create-items.md) | `POST /collections/:collection_id/items` | [docs](https://developers.webflow.com/data/reference/cms/collection-items/staged-items/create-item) |
| [Get Collection Details](actions/get-collection-details.md) | `GET /collections/:collection_id` | [docs](https://developers.webflow.com/data/reference/cms/collections/get) |
| [Get Component Content](actions/get-component-content.md) | `GET /sites/:site_id/components/:component_id/dom` | [docs](https://developers.webflow.com/data/reference/pages-and-components/components/get-content) |
| [Get Component Properties](actions/get-component-properties.md) | `GET /sites/:site_id/components/:component_id/properties` | [docs](https://developers.webflow.com/data/reference/pages-and-components/components/get-properties) |
| [Get Item](actions/get-item.md) | `GET /collections/:collection_id/items/:item_id` | [docs](https://developers.webflow.com/data/reference/cms/collection-items/staged-items/get-item) |
| [Get Page Content](actions/get-page-content.md) | `GET /pages/:page_id/dom` | [docs](https://developers.webflow.com/data/reference/pages-and-components/pages/get-content) |
| [Get Page Metadata](actions/get-page-metadata.md) | `GET /pages/:page_id` | [docs](https://developers.webflow.com/data/reference/pages-and-components/pages/get-metadata) |
| [Get Site](actions/get-site.md) | `GET /sites/:site_id` | [docs](https://developers.webflow.com/data/reference/sites/get) |
| [List Collections](actions/list-collections.md) | `GET /sites/:site_id/collections` | [docs](https://developers.webflow.com/data/reference/cms/collections/list) |
| [List Components](actions/list-components.md) | `GET /sites/:site_id/components` | [docs](https://developers.webflow.com/data/reference/pages-and-components/components/list) |
| [List Custom Domains](actions/list-custom-domains.md) | `GET /sites/:site_id/custom_domains` | [docs](https://developers.webflow.com/data/reference/sites/get-custom-domain) |
| [List Items](actions/list-items.md) | `GET /collections/:collection_id/items` | [docs](https://developers.webflow.com/data/reference/cms/collection-items/staged-items/list-items) |
| [List Pages](actions/list-pages.md) | `GET /sites/:site_id/pages` | [docs](https://developers.webflow.com/data/reference/pages-and-components/pages/list) |
| [List Sites](actions/list-sites.md) | `GET /sites` | [docs](https://developers.webflow.com/data/reference/sites/list) |
| [Publish Site](actions/publish-site.md) | `POST /sites/:site_id/publish` | [docs](https://developers.webflow.com/data/reference/sites/publish) |
| [Update Component Content](actions/update-component-content.md) | `POST /sites/:site_id/components/:component_id/dom` | [docs](https://developers.webflow.com/data/reference/pages-and-components/components/update-content) |
| [Update Component Properties](actions/update-component-properties.md) | `POST /sites/:site_id/components/:component_id/properties` | [docs](https://developers.webflow.com/data/reference/pages-and-components/components/update-properties) |
| [Update Page Content](actions/update-page-content.md) | `POST /pages/:page_id/dom` | [docs](https://developers.webflow.com/data/reference/pages-and-components/pages/update-static-content) |
| [Update Page Metadata](actions/update-page-metadata.md) | `PUT /pages/:page_id` | [docs](https://developers.webflow.com/data/reference/pages-and-components/pages/update-page-settings) |
