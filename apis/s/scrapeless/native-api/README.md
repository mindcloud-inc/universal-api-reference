# Scrapeless: Native API Reference

A consolidated summary of Scrapeless's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.scrapeless.com/
- **API base URL:** `https://api.scrapeless.com`

## Authentication

### API Key

Connect with your Scrapeless API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-token: <apiKey>
```

[Official authentication documentation](https://apidocs.scrapeless.com/api-11975058)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Cancel Batch Scrape Job](actions/cancel-batch-scrape-job.md) | `DELETE /api/v1/crawler/scrape/batch/:id` | [docs](https://apidocs.scrapeless.com/api-17509005) |
| [Cancel Crawl Job](actions/cancel-crawl-job.md) | `DELETE /api/v1/crawler/crawl/:id` | [docs](https://apidocs.scrapeless.com/api-17509008) |
| [Clear Browser Signals](actions/clear-browser-signals.md) | `DELETE /browser/:taskId/signal/clear` | [docs](https://apidocs.scrapeless.com/api-24795290) |
| [Configure 1Password Integration](actions/configure-1password-integration.md) | `PUT /browser/one-password/token` | [docs](https://apidocs.scrapeless.com/api-23850711) |
| [Create Batch Scrape Job](actions/create-batch-scrape-job.md) | `POST /api/v2/crawler/scrape/batch` | [docs](https://apidocs.scrapeless.com/api-17509003) |
| [Create Browser Profile](actions/create-browser-profile.md) | `POST /browser/profiles` | [docs](https://apidocs.scrapeless.com/api-19188049) |
| [Create Browser Session Task](actions/create-browser-session-task.md) | `GET /api/v2/browser` | [docs](https://apidocs.scrapeless.com/api-24826702) |
| [Create Crawl Job](actions/create-crawl-job.md) | `POST /api/v2/crawler/crawl` | [docs](https://apidocs.scrapeless.com/api-17509010) |
| [Create JS Render Request](actions/create-js-render-request.md) | `POST /api/v2/unlocker/request` | [docs](https://apidocs.scrapeless.com/api-12948840) |
| [Create Scrape Job](actions/create-scrape-job.md) | `POST /api/v2/crawler/scrape` | [docs](https://apidocs.scrapeless.com/api-17509002) |
| [Create Scraper Task](actions/create-scraper-task.md) | `POST /api/v1/scraper/request` | [docs](https://apidocs.scrapeless.com/api-11949852) |
| [Create Team Credential](actions/create-team-credential.md) | `POST /browser/credentials` | [docs](https://apidocs.scrapeless.com/api-23850715) |
| [Create Web Unlocker Request](actions/create-web-unlocker-request.md) | `POST /api/v2/unlocker/request` | [docs](https://apidocs.scrapeless.com/api-11949854) |
| [Delete Browser Extension](actions/delete-browser-extension.md) | `DELETE /browser/extensions/:extensionId` | [docs](https://apidocs.scrapeless.com/api-18350374) |
| [Delete Browser Profile](actions/delete-browser-profile.md) | `DELETE /browser/profiles/:profileId` | [docs](https://apidocs.scrapeless.com/api-19188051) |
| [Delete Team Credential](actions/delete-team-credential.md) | `DELETE /browser/credentials` | [docs](https://apidocs.scrapeless.com/api-23850717) |
| [Get 1Password Secret](actions/get-1password-secret.md) | `POST /browser/one-password/secret` | [docs](https://apidocs.scrapeless.com/api-23850713) |
| [Get 1Password Secrets](actions/get-1password-secrets.md) | `POST /browser/one-password/secrets` | [docs](https://apidocs.scrapeless.com/api-23850714) |
| [Get Batch Scrape Job Errors](actions/get-batch-scrape-job-errors.md) | `GET /api/v1/crawler/scrape/batch/:id/errors` | [docs](https://apidocs.scrapeless.com/api-17509006) |
| [Get Batch Scrape Job Status](actions/get-batch-scrape-job-status.md) | `GET /api/v1/crawler/scrape/batch/:id` | [docs](https://apidocs.scrapeless.com/api-17509004) |
| [Get Browser Extension](actions/get-browser-extension.md) | `GET /browser/extensions/:extensionId` | [docs](https://apidocs.scrapeless.com/api-18350563) |
| [Get Browser Profile](actions/get-browser-profile.md) | `GET /browser/profiles/:profileId` | [docs](https://apidocs.scrapeless.com/api-19188052) |
| [Get Browser Session Live URL](actions/get-browser-session-live-url.md) | `GET /browser/:taskId/live` | [docs](https://apidocs.scrapeless.com/api-16891208) |
| [Get Browser Signal Stats](actions/get-browser-signal-stats.md) | `GET /browser/:taskId/signal/stats` | [docs](https://apidocs.scrapeless.com/api-24795289) |
| [Get Crawl Job Errors](actions/get-crawl-job-errors.md) | `GET /api/v1/crawler/crawl/:id/errors` | [docs](https://apidocs.scrapeless.com/api-17509009) |
| [Get Crawl Job Status](actions/get-crawl-job-status.md) | `GET /api/v1/crawler/crawl/:id` | [docs](https://apidocs.scrapeless.com/api-17509007) |
| [Get Scrape Job Status](actions/get-scrape-job-status.md) | `GET /api/v1/crawler/scrape/:id` | [docs](https://apidocs.scrapeless.com/api-17644667) |
| [Get Scraper Result](actions/get-scraper-result.md) | `GET /api/v1/scraper/result/:taskId` | [docs](https://apidocs.scrapeless.com/api-11949853) |
| [Get Team Credential](actions/get-team-credential.md) | `GET /browser/credentials` | [docs](https://apidocs.scrapeless.com/api-23850718) |
| [Get User Info](actions/get-user-info.md) | `GET /api/v1/me` | [docs](https://apidocs.scrapeless.com/api-11949851) |
| [List Browser Extensions](actions/list-browser-extensions.md) | `GET /browser/extensions/list` | [docs](https://apidocs.scrapeless.com/api-18350572) |
| [List Browser Profiles](actions/list-browser-profiles.md) | `GET /browser/profiles` | [docs](https://apidocs.scrapeless.com/api-19188053) |
| [List Browser Signals](actions/list-browser-signals.md) | `GET /browser/:taskId/signal/list` | [docs](https://apidocs.scrapeless.com/api-24795288) |
| [List Running Browser Sessions](actions/list-running-browser-sessions.md) | `GET /browser/running` | [docs](https://apidocs.scrapeless.com/api-16890953) |
| [Revoke 1Password Authorization](actions/revoke-1password-authorization.md) | `DELETE /browser/one-password/token` | [docs](https://apidocs.scrapeless.com/api-23850712) |
| [Send Browser Signal](actions/send-browser-signal.md) | `POST /browser/:taskId/signal/send` | [docs](https://apidocs.scrapeless.com/api-24795286) |
| [Update Browser Extension](actions/update-browser-extension.md) | `PUT /browser/extensions/:extensionId` | [docs](https://apidocs.scrapeless.com/api-18350271) |
| [Update Browser Profile](actions/update-browser-profile.md) | `PUT /browser/profiles/:profileId` | [docs](https://apidocs.scrapeless.com/api-19188050) |
| [Update Team Credential](actions/update-team-credential.md) | `PUT /browser/credentials` | [docs](https://apidocs.scrapeless.com/api-23850716) |
| [Upload Browser Extension](actions/upload-browser-extension.md) | `POST /browser/extensions/upload` | [docs](https://apidocs.scrapeless.com/api-18350040) |
