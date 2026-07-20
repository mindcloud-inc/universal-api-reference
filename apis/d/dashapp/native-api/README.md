# Dash.app: Native API Reference

A consolidated summary of Dash.app's API configuration and 32 documented operations, with links to official documentation.

- **Official docs:** https://api-docs.dash.app/dash/openapi
- **OpenAPI specification:** https://api-docs.dash.app/_bundle/dash/@v2/openapi.yaml
- **API base URL:** `https://api-v2.dash.app`

## Authentication

### OAuth 2.0

Connect Dash with OAuth 2.0 authorization code and refresh tokens.

### Credentials

- **Subdomain:** `subdomain` · required · Your Dash account subdomain, for example my-account.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://login.dash.app/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://login.dash.app/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `offline_access subdomain:{{credentials.subdomain}}`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://login.dash.app/oauth/token.

[Official authentication documentation](https://api-docs.dash.app/dash/openapi/section/authorisation.md)

## API conventions

Responses from this API use JSON.

## Endpoints (32 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Asset Share](actions/create-asset-share.md) | `POST /asset-shares` | [docs](https://api-docs.dash.app/dash/openapi/asset-shares/createassetshare) |
| [Create Collection](actions/create-collection.md) | `POST /collections` | [docs](https://api-docs.dash.app/dash/openapi/collections/postcollection.md) |
| [Create Portal](actions/create-portal.md) | `POST /portals` | [docs](https://api-docs.dash.app/dash/openapi/portals/postportal) |
| [Create Saved Search](actions/create-saved-search.md) | `POST /saved-searches` | [docs](https://api-docs.dash.app/dash/openapi/saved-searches/postsavedsearch) |
| [Delete Asset Share](actions/delete-asset-share.md) | `DELETE /asset-shares/:id` | [docs](https://api-docs.dash.app/dash/openapi/asset-shares/deleteassetshare) |
| [Get Asset](actions/get-asset.md) | `GET /assets/:id` | [docs](https://api-docs.dash.app/dash/openapi/assets/getasset) |
| [Get Asset Files](actions/get-asset-files.md) | `GET /assets/:id/files` | [docs](https://api-docs.dash.app/dash/openapi/assets/getassetfiles) |
| [Get Asset Share](actions/get-asset-share.md) | `GET /asset-shares/:id` | [docs](https://api-docs.dash.app/dash/openapi/asset-shares/getassetshare) |
| [Get Corebook Settings](actions/get-corebook-settings.md) | `GET /corebook-settings` | [docs](https://api-docs.dash.app/dash/openapi/corebook/getcorebooksettings) |
| [Get Current User](actions/get-current-user.md) | `GET /current-user` | [docs](https://api-docs.dash.app/dash/openapi/users/getcurrentuser.md) |
| [Get Field](actions/get-field.md) | `GET /fields/:id` | [docs](https://api-docs.dash.app/dash/openapi/fields/getfield) |
| [Get Field Option](actions/get-field-option.md) | `GET /field-options/:id` | [docs](https://api-docs.dash.app/dash/openapi/field-options/getfieldoption) |
| [Get Field Views](actions/get-field-views.md) | `GET /field-views` | [docs](https://api-docs.dash.app/dash/openapi/field-views/getfieldviews) |
| [Get Fields](actions/get-fields.md) | `GET /fields` | [docs](https://api-docs.dash.app/dash/openapi/fields/getfields) |
| [Get Folder Settings](actions/get-folder-settings.md) | `GET /folder-settings` | [docs](https://api-docs.dash.app/dash/openapi/folder-settings/getfoldersettings) |
| [Get Group](actions/get-group.md) | `GET /groups/:id` | [docs](https://api-docs.dash.app/dash/openapi/users/getgroup) |
| [Get Grouped Preset Transformations](actions/get-grouped-preset-transformations.md) | `GET /grouped-preset-transformations` | [docs](https://api-docs.dash.app/dash/openapi/preset-transformations/getgroupedpresettransformations) |
| [Get Groups](actions/get-groups.md) | `GET /groups` | [docs](https://api-docs.dash.app/dash/openapi/users/getgroups) |
| [Get Portal](actions/get-portal.md) | `GET /portals/:id` | [docs](https://api-docs.dash.app/dash/openapi/portals/getportal) |
| [Get Saved Search](actions/get-saved-search.md) | `GET /saved-searches/:id` | [docs](https://api-docs.dash.app/dash/openapi/saved-searches/getsavedsearch) |
| [Get Search Filter View](actions/get-search-filter-view.md) | `GET /search-filter-view` | [docs](https://api-docs.dash.app/dash/openapi/search-filters/getsearchfilterview) |
| [Get User](actions/get-user.md) | `GET /users/:id` | [docs](https://api-docs.dash.app/dash/openapi/users/getuser.md) |
| [Search Asset Download Events](actions/search-asset-download-events.md) | `POST /asset-download-event-searches` | [docs](https://api-docs.dash.app/dash/openapi/asset-download-events/postassetdownloadeventsearch) |
| [Search Assets](actions/search-assets.md) | `POST /asset-searches` | [docs](https://api-docs.dash.app/dash/openapi/assets/postassetsearch) |
| [Search Collections](actions/search-collections.md) | `POST /collection-searches` | [docs](https://api-docs.dash.app/dash/openapi/collections/postcollectionsearch) |
| [Search Field Options](actions/search-field-options.md) | `POST /field-option-searches` | [docs](https://api-docs.dash.app/dash/openapi/field-options/postfieldoptionsearch) |
| [Search Portals](actions/search-portals.md) | `POST /portal-searches` | [docs](https://api-docs.dash.app/dash/openapi/portals/postportalsearch) |
| [Search Preset Transformations](actions/search-preset-transformations.md) | `POST /preset-transformation-searches` | [docs](https://api-docs.dash.app/dash/openapi/preset-transformations/postpresettransformationsearch) |
| [Search Saved Searches](actions/search-saved-searches.md) | `POST /saved-search-searches` | [docs](https://api-docs.dash.app/dash/openapi/saved-searches/postsavedsearchsearch) |
| [Search Themes](actions/search-themes.md) | `POST /theme-searches` | [docs](https://api-docs.dash.app/dash/openapi/theme/postthemesearch) |
| [Search Users](actions/search-users.md) | `POST /user-searches` | [docs](https://api-docs.dash.app/dash/openapi/users/postusersearch) |
| [Update Asset Share](actions/update-asset-share.md) | `PATCH /asset-shares/:id` | [docs](https://api-docs.dash.app/dash/openapi/asset-shares/patchassetshare) |
