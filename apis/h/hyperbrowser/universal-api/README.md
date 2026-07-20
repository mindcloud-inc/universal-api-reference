# <img src="https://images.mindcloud.co/apps/icons/hyperbrowser_1774291749161.png" alt="Hyperbrowser logo" width="28" height="28"> Hyperbrowser: Universal API

Browse, scrape, search, and automate the web

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/hyperbrowser/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.hyperbrowser.ai
- **Vendor API docs:** https://www.hyperbrowser.ai/docs/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Fetch Web Page](actions/fetch-web-page.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/fetch-web-page?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Browser Use Task

| Action | Method | Description |
| --- | --- | --- |
| [Get Browser Use Task Status and Results](actions/get-browser-use-task-status-and-results.md) | GET |  |
| [Start Browser Use Task](actions/start-browser-use-task.md) | POST |  |
| [Stop Browser Use Task](actions/stop-browser-use-task.md) | PUT |  |

### Crawl Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Crawl Job Status and Results](actions/get-crawl-job-status-and-results.md) | GET |  |
| [Start Crawl Job](actions/start-crawl-job.md) | POST |  |

### Extract Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Extract Job Status and Results](actions/get-extract-job-status-and-results.md) | GET |  |
| [Start Extract Job](actions/start-extract-job.md) | POST |  |

### Hyperagent Task

| Action | Method | Description |
| --- | --- | --- |
| [Get HyperAgent Task Status and Results](actions/get-hyperagent-task-status-and-results.md) | GET |  |
| [Start HyperAgent Task](actions/start-hyperagent-task.md) | POST |  |
| [Stop HyperAgent Task](actions/stop-hyperagent-task.md) | PUT |  |

### Profile

| Action | Method | Description |
| --- | --- | --- |
| [Create Profile](actions/create-profile.md) | POST |  |
| [Delete Profile](actions/delete-profile.md) | DELETE |  |
| [Get Profile](actions/get-profile.md) | GET |  |
| [List Profiles](actions/list-profiles.md) | GET |  |

### Scrape Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Scrape Job](actions/create-scrape-job.md) | POST |  |
| [Get Scrape Job Status and Result](actions/get-scrape-job-status-and-result.md) | GET |  |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search the Web](actions/search-the-web.md) | GET |  |

### Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Session](actions/create-session.md) | POST |  |
| [Get Session](actions/get-session.md) | GET |  |
| [List Sessions](actions/list-sessions.md) | GET |  |
| [Stop Session](actions/stop-session.md) | PUT |  |

### Web Crawl Job

| Action | Method | Description |
| --- | --- | --- |
| [Get Web Crawl Job Results](actions/get-web-crawl-job-results.md) | GET |  |
| [Start Web Crawl Job](actions/start-web-crawl-job.md) | POST |  |

### Web Page

| Action | Method | Description |
| --- | --- | --- |
| [Fetch Web Page](actions/fetch-web-page.md) | GET |  |

