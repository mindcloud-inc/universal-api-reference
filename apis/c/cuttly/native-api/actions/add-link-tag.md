# Add Link Tag with Cutt.ly

Adds a tag to a shortened link in Cutt.ly.

## Endpoint

- **Method:** `GET`
- **Path:** `/api.php`
- **Base URL:** `https://cutt.ly/api`
- **Official documentation:** [Add Link Tag](https://cutt.ly/api-documentation/cuttly-links-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `edit` | query | `string` | yes | The short link to edit. |
| `tag` | query | `string` | yes | Tag to assign to the short link. |
