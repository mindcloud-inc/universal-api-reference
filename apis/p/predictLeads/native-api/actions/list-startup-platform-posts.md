# List Startup Platform Posts with PredictLeads

Retrieves startup platform posts from the PredictLeads API.

## Endpoint

- **Method:** `GET`
- **Path:** `/discover/startup_platform_posts`
- **Base URL:** `https://predictleads.com/api/v3`
- **Official documentation:** [List Startup Platform Posts](https://docs.predictleads.com/api_endpoints/startup_platform_posts_dataset/retrieve_latest_posts)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `published_at_from` | query | `date` | no | Only return startup platform posts published after the given date (ISO 8601). |
| `published_at_until` | query | `date` | no | Only return startup platform posts published before the given date (ISO 8601). |
| `post_types` | query | `string` | no | Comma-separated startup platform post types. Supported values: show_hn, job_hn. Send multiple values as a string separated by `,`. |
| `page` | query | `number` | no | Page number of shown items. |
| `limit` | query | `number` | no | Limit the number of shown items per page. |
