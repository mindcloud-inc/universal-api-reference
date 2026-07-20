# <img src="https://images.mindcloud.co/apps/icons/id-l5txeq-ow-1776732337887_1776732450806.png" alt="Datastreamer logo" width="28" height="28"> Datastreamer: Universal API

Ingest, enrich, and search data across dynamic pipelines

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/datastreamer/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://datastreamer.io
- **Vendor API docs:** https://docs.datastreamer.io/docs/welcome-to-datastreamer

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Search Jobs](actions/search-jobs.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datastreamer/latest/actions/search-jobs?connectionId=$CONNECTION_ID&query=%5Bobject%20Object%5D&query.query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Job

| Action | Method | Description |
| --- | --- | --- |
| [Search Jobs](actions/search-jobs.md) | GET | Finds jobs in Datastreamer by Lucene query. |

### Jobs

| Action | Method | Description |
| --- | --- | --- |
| [Create Bluesky Live Feed Job](actions/create-bluesky-live-feed-job.md) | POST | Creates a Bluesky live feed job in Datastreamer. |
| [Create DarkOwl Search Job](actions/create-dark-owl-search-job.md) | POST | Creates a DarkOwl search job in Datastreamer. |
| [Create Data365 Facebook Posts Search Job](actions/create-data365-facebook-posts-search-job.md) | POST | Creates a Data365 Facebook posts search job in Datastreamer. |
| [Create Data365 Instagram Profile Feed Posts Job](actions/create-data365-instagram-profile-feed-posts-job.md) | POST | Creates a Data365 Instagram profile feed posts job in Datastreamer. |
| [Create Data365 Instagram Profile Search Job](actions/create-data365-instagram-profile-search-job.md) | POST | Creates a Data365 Instagram profile search job in Datastreamer. |
| [Create Data365 TikTok Keywords Job](actions/create-data365-tik-tok-keywords-job.md) | POST | Creates a Data365 TikTok keyword search job in Datastreamer. |
| [Create Data365 X Keywords Job](actions/create-data365-x-keywords-job.md) | POST | Creates a Data365 X keyword search job in Datastreamer. |
| [Create Job](actions/create-job.md) | POST | Creates a new job in Datastreamer. |
| [Create Opoint News Job](actions/create-opoint-news-job.md) | POST | Creates an Opoint News search job in Datastreamer. |
| [Create Searchable Storage Aggregate Job](actions/create-searchable-storage-aggregate-job.md) | POST | Creates a Searchable Storage aggregate job in Datastreamer. |
| [Create Searchable Storage Combined Search And Aggregate Job](actions/create-searchable-storage-combined-search-and-aggregate-job.md) | POST | Creates a Searchable Storage search-and-aggregate job in Datastreamer. |
| [Create Searchable Storage Search Job](actions/create-searchable-storage-search-job.md) | POST | Creates a Searchable Storage search job in Datastreamer. |
| [Create Socialgist Blogs Job](actions/create-socialgist-blogs-job.md) | POST | Creates a Socialgist Blogs job in Datastreamer. |
| [Create Socialgist Boards Job](actions/create-socialgist-boards-job.md) | POST | Creates a Socialgist Boards job in Datastreamer. |
| [Create Socialgist News Job](actions/create-socialgist-news-job.md) | POST | Creates a Socialgist News job in Datastreamer. |
| [Create Socialgist Reddit Job](actions/create-socialgist-reddit-job.md) | POST | Creates a Socialgist Reddit job in Datastreamer. |
| [Create Socialgist TikTok Job](actions/create-socialgist-tik-tok-job.md) | POST | Creates a Socialgist TikTok job in Datastreamer. |
| [Create WebSightLine Augmented Instagram Job](actions/create-web-sight-line-augmented-instagram-job.md) | POST | Creates a WebSightLine augmented Instagram search job in Datastreamer. |
| [Create WebSightLine Instagram Job](actions/create-web-sight-line-instagram-job.md) | POST | Creates a WebSightLine Instagram search job in Datastreamer. |
| [Create WebSightLine Threads Job](actions/create-web-sight-line-threads-job.md) | POST | Creates a WebSightLine Threads job in Datastreamer. |
| [List Jobs](actions/list-jobs.md) | GET | Retrieves previously created jobs from Datastreamer. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Count Job DVU Usage](actions/count-job-dvu-usage.md) | GET | Retrieves DVU usage for jobs from Datastreamer. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Search Work Items](actions/search-work-items.md) | GET |  |

