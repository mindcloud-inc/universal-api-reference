# Queue Article with SEOTakeoff

## Endpoint

- **Method:** `POST`
- **Path:** `/api/zapier/articles/queue`
- **Base URL:** `https://api.seotakeoff.com`
- **Official documentation:** [Queue Article](https://api.seotakeoff.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `keyword` | body | `string` | yes | Target SEO keyword for the queued article. |
| `website_id` | body | `string` | yes | Website ID from List Websites. |
| `title` | body | `string` | no | Optional custom article title. |
| `cluster_id` | body | `string` | no | Optional cluster ID to associate with the article. |
| `priority` | body | `string` | no | Optional priority: high, normal, or low. |
