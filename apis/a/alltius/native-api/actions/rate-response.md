# Rate Response with Alltius

Updates feedback for an Alltius assistant response.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/chat/rating`
- **Base URL:** `https://app.alltius.ai/api/platform`
- **Official documentation:** [Rate Response](https://app.alltius.ai/api/platform/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `post_id` | body | `string` | yes | — |
| `rating` | body | `number` | yes | Use 1 for thumbs up or -1 for thumbs down. |
