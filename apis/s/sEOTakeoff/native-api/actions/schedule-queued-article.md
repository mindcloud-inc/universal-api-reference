# Schedule Queued Article with SEOTakeoff

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/article-queue/schedule`
- **Base URL:** `https://api.seotakeoff.com`
- **Official documentation:** [Schedule Queued Article](https://api.seotakeoff.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `queue_item_id` | body | `number` | yes | Queued article ID from Queue Article. |
| `scheduled_date` | body | `date` | yes | Date to schedule the queued article. |
