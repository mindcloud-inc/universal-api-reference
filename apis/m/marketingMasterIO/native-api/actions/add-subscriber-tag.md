# Add Subscriber Tag with Marketing Master IO

Adds a tag to a Messenger subscriber in Marketing Master IO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/messenger/subscriber/:subscriber_id/tags/:tag`
- **Base URL:** `https://api.marketingmaster.io`
- **Official documentation:** [Add Subscriber Tag](https://developers.marketingmaster.io/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subscriber_id` | path | `string` | yes |
| `tag` | path | `string` | yes |
