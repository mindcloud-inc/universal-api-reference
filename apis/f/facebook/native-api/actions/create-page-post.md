# Create Page Post with Facebook

## Endpoint

- **Method:** `POST`
- **Path:** `/:pageId/feed`
- **Base URL:** `https://graph.facebook.com/v25.0`
- **Official documentation:** [Create Page Post](https://developers.facebook.com/docs/graph-api/reference/page/feed/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pageId` | path | `list<string>` | yes | — |
| `message` | body | `string` | no | — |
| `link` | body | `string` | no | URL to attach. Provide Message, Link, or both. |
| `published` | body | `boolean` | no | Set to false to create an unpublished post. |
| `scheduled_publish_time` | body | `date` | no | 10 minutes to 75 days from now. Set Published to false when scheduling. |
