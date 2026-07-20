# Netlify: Native API Reference

A consolidated summary of Netlify's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://open-api.netlify.com/
- **OpenAPI specification:** https://open-api.netlify.com/swagger.json
- **API base URL:** `https://api.netlify.com/api/v1`

## Authentication

### OAuth2

OAuth2 authentication for Netlify API access.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://app.netlify.com/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.netlify.com/oauth/token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


[Official authentication documentation](https://docs.netlify.com/manage/accounts-and-teams/user-settings-and-permissions/#oauth-applications)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Site Deploy](actions/cancel-site-deploy.md) | `POST /deploys/:deploy_id/cancel` | [docs](https://open-api.netlify.com/#operation/cancelSiteDeploy) |
| [Configure DNS for Site](actions/configure-dns-for-site.md) | `PUT /sites/:site_id/dns` | [docs](https://open-api.netlify.com/#operation/configureDNSForSite) |
| [Create Environment Variables](actions/create-environment-variables.md) | `POST /accounts/:account_id/env` | [docs](https://open-api.netlify.com/#operation/createEnvVars) |
| [Create Site](actions/create-site.md) | `POST /sites` | [docs](https://open-api.netlify.com/#operation/createSite) |
| [Create Site Build Hook](actions/create-site-build-hook.md) | `POST /sites/:site_id/build_hooks` | [docs](https://open-api.netlify.com/#operation/createSiteBuildHook) |
| [Create Site Deploy](actions/create-site-deploy.md) | `POST /sites/:site_id/deploys` | [docs](https://open-api.netlify.com/#operation/createSiteDeploy) |
| [Delete Environment Variable](actions/delete-environment-variable.md) | `DELETE /accounts/:account_id/env/:key` | [docs](https://open-api.netlify.com/#operation/deleteEnvVar) |
| [Delete Site](actions/delete-site.md) | `DELETE /sites/:site_id` | [docs](https://open-api.netlify.com/#operation/deleteSite) |
| [Delete Site Build Hook](actions/delete-site-build-hook.md) | `DELETE /sites/:site_id/build_hooks/:id` | [docs](https://open-api.netlify.com/#operation/deleteSiteBuildHook) |
| [Disable Site](actions/disable-site.md) | `PUT /sites/:site_id/disable` | [docs](https://open-api.netlify.com/#operation/disableSite) |
| [Enable Site](actions/enable-site.md) | `PUT /sites/:site_id/enable` | [docs](https://open-api.netlify.com/#operation/enableSite) |
| [Get DNS for Site](actions/get-dns-for-site.md) | `GET /sites/:site_id/dns` | [docs](https://open-api.netlify.com/#operation/getDNSForSite) |
| [Get Environment Variable](actions/get-environment-variable.md) | `GET /accounts/:account_id/env/:key` | [docs](https://open-api.netlify.com/#operation/getEnvVar) |
| [Get Site](actions/get-site.md) | `GET /sites/:site_id` | [docs](https://open-api.netlify.com/#operation/getSite) |
| [Get Site Build](actions/get-site-build.md) | `GET /builds/:build_id` | [docs](https://open-api.netlify.com/#operation/getSiteBuild) |
| [Get Site Deploy](actions/get-site-deploy.md) | `GET /sites/:site_id/deploys/:deploy_id` | [docs](https://open-api.netlify.com/#operation/getSiteDeploy) |
| [List Environment Variables](actions/list-environment-variables.md) | `GET /accounts/:account_id/env` | [docs](https://open-api.netlify.com/#operation/getEnvVars) |
| [List Form Submissions](actions/list-form-submissions.md) | `GET /forms/:form_id/submissions` | [docs](https://open-api.netlify.com/#operation/listFormSubmissions) |
| [List Site Build Hooks](actions/list-site-build-hooks.md) | `GET /sites/:site_id/build_hooks` | [docs](https://open-api.netlify.com/#operation/listSiteBuildHooks) |
| [List Site Builds](actions/list-site-builds.md) | `GET /sites/:site_id/builds` | [docs](https://open-api.netlify.com/#operation/listSiteBuilds) |
| [List Site Deploys](actions/list-site-deploys.md) | `GET /sites/:site_id/deploys` | [docs](https://open-api.netlify.com/#operation/listSiteDeploys) |
| [List Site Forms](actions/list-site-forms.md) | `GET /sites/:site_id/forms` | [docs](https://open-api.netlify.com/#operation/listSiteForms) |
| [List Site Submissions](actions/list-site-submissions.md) | `GET /sites/:site_id/submissions` | [docs](https://open-api.netlify.com/#operation/listSiteSubmissions) |
| [List Sites](actions/list-sites.md) | `GET /sites` | [docs](https://open-api.netlify.com/#operation/listSites) |
| [Restore Site Deploy](actions/restore-site-deploy.md) | `POST /sites/:site_id/deploys/:deploy_id/restore` | [docs](https://open-api.netlify.com/#operation/restoreSiteDeploy) |
| [Rollback Site Deploy](actions/rollback-site-deploy.md) | `PUT /sites/:site_id/rollback` | [docs](https://open-api.netlify.com/#operation/rollbackSiteDeploy) |
| [Search Site Functions](actions/search-site-functions.md) | `GET /sites/:site_id/functions` | [docs](https://open-api.netlify.com/#operation/searchSiteFunctions) |
| [Update Environment Variable](actions/update-environment-variable.md) | `PUT /accounts/:account_id/env/:key` | [docs](https://open-api.netlify.com/#operation/updateEnvVar) |
| [Update Site](actions/update-site.md) | `PATCH /sites/:site_id` | [docs](https://open-api.netlify.com/#operation/updateSite) |
| [Update Site Build Hook](actions/update-site-build-hook.md) | `PUT /sites/:site_id/build_hooks/:id` | [docs](https://open-api.netlify.com/#operation/updateSiteBuildHook) |
