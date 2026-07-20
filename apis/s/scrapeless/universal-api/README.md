# <img src="https://images.mindcloud.co/apps/icons/scrapeless_1775750856021.png" alt="Scrapeless logo" width="28" height="28"> Scrapeless: Universal API

Scrape websites, manage browser sessions, and extract structured data

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/scrapeless/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.scrapeless.com
- **Vendor API docs:** https://apidocs.scrapeless.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get User Info](actions/get-user-info.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### 1password Integration

| Action | Method | Description |
| --- | --- | --- |
| [Configure 1Password Integration](actions/configure-1password-integration.md) | PUT | Updates the 1Password integration in Scrapeless. |
| [Revoke 1Password Authorization](actions/revoke-1password-authorization.md) | DELETE | Deletes the 1Password authorization from Scrapeless. |

### 1password Secret

| Action | Method | Description |
| --- | --- | --- |
| [Get 1Password Secret](actions/get-1password-secret.md) | GET | Retrieves a 1Password secret from Scrapeless. |
| [Get 1Password Secrets](actions/get-1password-secrets.md) | GET | Retrieves 1Password secrets from Scrapeless. |

### Browser Extension

| Action | Method | Description |
| --- | --- | --- |
| [Delete Browser Extension](actions/delete-browser-extension.md) | DELETE | Deletes a browser extension from Scrapeless. |
| [Get Browser Extension](actions/get-browser-extension.md) | GET | Retrieves a browser extension from Scrapeless. |
| [List Browser Extensions](actions/list-browser-extensions.md) | GET | Retrieves browser extensions from Scrapeless. |
| [Update Browser Extension](actions/update-browser-extension.md) | PUT | Updates an existing browser extension in Scrapeless. |
| [Upload Browser Extension](actions/upload-browser-extension.md) | POST | Uploads a browser extension to Scrapeless. |

### Browser Profile

| Action | Method | Description |
| --- | --- | --- |
| [Create Browser Profile](actions/create-browser-profile.md) | POST | Creates a new browser profile in Scrapeless. |
| [Delete Browser Profile](actions/delete-browser-profile.md) | DELETE | Deletes a browser profile from Scrapeless. |
| [Get Browser Profile](actions/get-browser-profile.md) | GET | Retrieves a browser profile from Scrapeless. |
| [List Browser Profiles](actions/list-browser-profiles.md) | GET | Retrieves browser profiles from Scrapeless. |
| [Update Browser Profile](actions/update-browser-profile.md) | PUT | Updates an existing browser profile in Scrapeless. |

### Browser Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Browser Session Task](actions/create-browser-session-task.md) | POST | Creates a browser session task in Scrapeless. |
| [Get Browser Session Live URL](actions/get-browser-session-live-url.md) | GET | Retrieves a browser session live URL from Scrapeless. |
| [List Running Browser Sessions](actions/list-running-browser-sessions.md) | GET | Retrieves running browser sessions from Scrapeless. |

### Browser Signal

| Action | Method | Description |
| --- | --- | --- |
| [Clear Browser Signals](actions/clear-browser-signals.md) | DELETE | Deletes browser signals from Scrapeless. |
| [Get Browser Signal Stats](actions/get-browser-signal-stats.md) | GET | Retrieves browser signal stats from Scrapeless. |
| [List Browser Signals](actions/list-browser-signals.md) | GET | Retrieves browser signals from Scrapeless. |
| [Send Browser Signal](actions/send-browser-signal.md) | POST | Creates a browser signal in Scrapeless. |

### Crawl Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Crawl Job](actions/cancel-crawl-job.md) | DELETE | Deletes a crawl job from Scrapeless. |
| [Create Crawl Job](actions/create-crawl-job.md) | POST | Creates a new crawl job in Scrapeless. |
| [Get Crawl Job Errors](actions/get-crawl-job-errors.md) | GET | Retrieves crawl job errors from Scrapeless. |
| [Get Crawl Job Status](actions/get-crawl-job-status.md) | GET | Retrieves a crawl job status from Scrapeless. |

### Scrape Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Batch Scrape Job](actions/cancel-batch-scrape-job.md) | DELETE | Deletes a batch scrape job from Scrapeless. |
| [Create Batch Scrape Job](actions/create-batch-scrape-job.md) | POST | Creates a new batch scrape job in Scrapeless. |
| [Create Scrape Job](actions/create-scrape-job.md) | POST | Creates a new scrape job in Scrapeless. |
| [Get Batch Scrape Job Errors](actions/get-batch-scrape-job-errors.md) | GET | Retrieves batch scrape job errors from Scrapeless. |
| [Get Batch Scrape Job Status](actions/get-batch-scrape-job-status.md) | GET | Retrieves a batch scrape job status from Scrapeless. |
| [Get Scrape Job Status](actions/get-scrape-job-status.md) | GET | Retrieves a scrape job status from Scrapeless. |

### Scraper Task

| Action | Method | Description |
| --- | --- | --- |
| [Create Scraper Task](actions/create-scraper-task.md) | POST | Creates a new scraper task in Scrapeless. |
| [Get Scraper Result](actions/get-scraper-result.md) | GET | Retrieves a scraper result from Scrapeless. |

### Team Credential

| Action | Method | Description |
| --- | --- | --- |
| [Create Team Credential](actions/create-team-credential.md) | POST | Creates a new team credential in Scrapeless. |
| [Delete Team Credential](actions/delete-team-credential.md) | DELETE | Deletes a team credential from Scrapeless. |
| [Get Team Credential](actions/get-team-credential.md) | GET | Retrieves a team credential from Scrapeless. |
| [Update Team Credential](actions/update-team-credential.md) | PUT | Updates an existing team credential in Scrapeless. |

### Unlocker Request

| Action | Method | Description |
| --- | --- | --- |
| [Create JS Render Request](actions/create-js-render-request.md) | POST | Creates a JS render request in Scrapeless. |
| [Create Web Unlocker Request](actions/create-web-unlocker-request.md) | POST | Creates a web unlocker request in Scrapeless. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User Info](actions/get-user-info.md) | GET | Retrieves user information from Scrapeless. |

