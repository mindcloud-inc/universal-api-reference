# Get Videos Analytics with Teyuto

Retrieves video analytics from a Teyuto channel.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics/videos`
- **Base URL:** `https://api.teyuto.tv/v2`
- **Official documentation:** [Get Videos Analytics](https://apidocs.teyuto.com/api-9259147)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `end_date` | query | `string` | no | Analytics window end |
| `start_date` | query | `string` | no | Analytics window start |
| `tag_id` | query | `string` | no | Tag to scope video analytics to |
