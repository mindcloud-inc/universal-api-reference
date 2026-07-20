# Get Collections Analytics with Teyuto

Retrieves collection analytics from a Teyuto channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics/collections`
- **Base URL:** `https://api.teyuto.tv/v2`
- **Official documentation:** [Get Collections Analytics](https://apidocs.teyuto.com/api-9259145)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | query | `string` | no | Analytics window end |
| `start_date` | query | `string` | no | Analytics window start |
| `tag_id` | query | `string` | no | Tag to scope collection analytics to |
| `user_id` | query | `string` | no | User to scope collection analytics to |
