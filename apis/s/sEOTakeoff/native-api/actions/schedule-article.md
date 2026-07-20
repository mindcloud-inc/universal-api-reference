# Schedule Article with SEOTakeoff

## Endpoint

- **Method:** `POST`
- **Path:** `/api/zapier/articles/schedule`
- **Base URL:** `https://api.seotakeoff.com`
- **Official documentation:** [Schedule Article](https://api.seotakeoff.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `article_id` | body | `string` | yes | Article ID from Generate Article or Search Articles. |
| `scheduled_date` | body | `string` | no | Optional ISO date to publish the article. |
| `scheduled_time` | body | `string` | no | Optional 24-hour time like 09:00. |
