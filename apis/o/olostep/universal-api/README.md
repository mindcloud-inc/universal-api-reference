# <img src="https://images.mindcloud.co/apps/icons/olostep_1774290111004.png" alt="Olostep logo" width="28" height="28"> Olostep: Universal API

Search, scrape, crawl, and structure web data with Olostep's Web Data API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/olostep/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 23
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.olostep.com
- **Vendor API docs:** https://docs.olostep.com/api-reference/common/object-oriented

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Answer](actions/get-answer.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/olostep/latest/actions/get-answer?connectionId=$CONNECTION_ID&answerId=answer_123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (23)

### Answer

| Action | Method | Description |
| --- | --- | --- |
| [Create Answer](actions/create-answer.md) | POST | Creates a new answer in Olostep. |
| [Get Answer](actions/get-answer.md) | GET | Retrieves details for an answer in Olostep. |

### Batch

| Action | Method | Description |
| --- | --- | --- |
| [Create Batch](actions/create-batch.md) | POST | Creates a new batch in Olostep. |
| [Get Batch](actions/get-batch.md) | GET | Retrieves details for a batch in Olostep. |

### Batch Item

| Action | Method | Description |
| --- | --- | --- |
| [List Batch Items](actions/list-batch-items.md) | GET | Retrieves items from an Olostep batch. |

### Content

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Content](actions/retrieve-content.md) | GET | Retrieves content by retrieve ID from Olostep. |

### Crawl

| Action | Method | Description |
| --- | --- | --- |
| [Create Crawl](actions/create-crawl.md) | POST | Creates a new crawl in Olostep. |
| [Get Crawl](actions/get-crawl.md) | GET | Retrieves details for a crawl in Olostep. |

### Crawl Page

| Action | Method | Description |
| --- | --- | --- |
| [List Crawl Pages](actions/list-crawl-pages.md) | GET | Retrieves pages from an Olostep crawl. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Complete File Upload](actions/complete-file-upload.md) | PUT | Completes a file upload in Olostep. |
| [Create File Upload](actions/create-file-upload.md) | POST | Creates a new file upload in Olostep. |
| [Delete File](actions/delete-file.md) | DELETE | Deletes an existing file from Olostep. |
| [Get File](actions/get-file.md) | GET | Retrieves details for a file in Olostep. |

### Map

| Action | Method | Description |
| --- | --- | --- |
| [Create Map](actions/create-map.md) | POST | Creates a new map in Olostep. |
| [Get Map](actions/get-map.md) | GET | Retrieves details for a map in Olostep. |

### Schedule

| Action | Method | Description |
| --- | --- | --- |
| [Create Schedule](actions/create-schedule.md) | POST | Creates a new schedule in Olostep. |
| [Delete Schedule](actions/delete-schedule.md) | DELETE | Deletes an existing schedule from Olostep. |
| [Get Schedule](actions/get-schedule.md) | GET | Retrieves details for a schedule in Olostep. |
| [List Schedules](actions/list-schedules.md) | GET | Retrieves schedules from Olostep. |

### Scrape

| Action | Method | Description |
| --- | --- | --- |
| [Create Scrape](actions/create-scrape.md) | POST | Creates a new scrape in Olostep. |
| [Get Scrape](actions/get-scrape.md) | GET | Retrieves details for a scrape in Olostep. |

### Search

| Action | Method | Description |
| --- | --- | --- |
| [Create Search](actions/create-search.md) | POST | Creates a new search in Olostep. |
| [Get Search](actions/get-search.md) | GET | Retrieves details for a search in Olostep. |

