# <img src="https://images.mindcloud.co/apps/icons/webcrawler-api_1774457140063.png" alt="Webcrawler API logo" width="28" height="28"> Webcrawler API: Universal API

Scrape websites, crawl pages, and monitor content changes

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/webcrawlerAPI/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://webcrawlerapi.com
- **Vendor API docs:** https://webcrawlerapi.com/docs/getting-started

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Feeds](actions/list-feeds.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webcrawlerAPI/latest/actions/list-feeds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Api Status

| Action | Method | Description |
| --- | --- | --- |
| [Ping API](actions/ping-api.md) | GET | Retrieves API availability status from Webcrawler API. |

### Authentication Status

| Action | Method | Description |
| --- | --- | --- |
| [Check Authentication](actions/check-authentication.md) | GET | Retrieves authentication status from Webcrawler API. |

### Crawl Job

| Action | Method | Description |
| --- | --- | --- |
| [Cancel Crawl Job](actions/cancel-crawl-job.md) | PUT | Cancels an existing crawl job in Webcrawler API. |
| [Create Crawl Job](actions/create-crawl-job.md) | POST | Creates a website crawl job in Webcrawler API. |
| [Get Crawl Job](actions/get-crawl-job.md) | GET | Retrieves crawl job status and results from Webcrawler API. |

### Crawl Job Url Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Crawl Job URLs](actions/get-crawl-job-urls.md) | GET | Retrieves discovered URLs for a crawl job in Webcrawler API. |

### Feed

| Action | Method | Description |
| --- | --- | --- |
| [Create Feed](actions/create-feed.md) | POST | Creates a scheduled website monitoring feed in Webcrawler API. |
| [Delete Feed](actions/delete-feed.md) | DELETE | Deletes an existing feed from Webcrawler API. |
| [Force Run Feed](actions/force-run-feed.md) | PUT | Triggers an immediate feed run in Webcrawler API. |
| [Get Feed](actions/get-feed.md) | GET | Retrieves feed details and recent runs from Webcrawler API. |
| [List Feeds](actions/list-feeds.md) | GET | Retrieves all feeds for your organization from Webcrawler API. |
| [Pause Feed](actions/pause-feed.md) | PUT | Pauses an existing feed in Webcrawler API. |
| [Resume Feed](actions/resume-feed.md) | PUT | Resumes a paused feed in Webcrawler API. |

### Feed Item

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed JSON](actions/get-feed-json.md) | GET | Retrieves feed changes in JSON Feed format from Webcrawler API. |

### Feed Rss

| Action | Method | Description |
| --- | --- | --- |
| [Get Feed RSS](actions/get-feed-rss.md) | GET | Retrieves feed changes in Atom format from Webcrawler API. |

### Organization Usage

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Usage](actions/get-organization-usage.md) | GET | Retrieves organization usage statistics from Webcrawler API. |

### Scrape Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Scrape Job](actions/create-scrape-job.md) | POST | Creates a single-page scrape job in Webcrawler API. |

### Scrape Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Scrape Job](actions/get-scrape-job.md) | GET | Retrieves scrape job status and results from Webcrawler API. |

### Webhook Delivery

| Action | Method | Description |
| --- | --- | --- |
| [Resend Crawl Job Webhook](actions/resend-crawl-job-webhook.md) | PUT | Resends a crawl job webhook from Webcrawler API. |
| [Resend Feed Webhook](actions/resend-feed-webhook.md) | PUT | Resends a feed webhook from Webcrawler API. |

