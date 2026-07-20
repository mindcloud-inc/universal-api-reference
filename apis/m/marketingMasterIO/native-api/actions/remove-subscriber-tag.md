# Remove Subscriber Tag with Marketing Master IO

Removes a tag from a Messenger subscriber in Marketing Master IO.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/messenger/subscriber/:subscriber_id/tags/:tag`
- **Base URL:** `https://api.marketingmaster.io`
- **Official documentation:** [Remove Subscriber Tag](https://developers.marketingmaster.io/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `subscriber_id` | path | `string` | yes |
| `tag` | path | `string` | yes |
