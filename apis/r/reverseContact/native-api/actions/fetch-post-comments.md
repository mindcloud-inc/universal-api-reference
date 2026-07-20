# Fetch Post Comments with Reverse Contact

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/fetch/posts/comments/live`
- **Base URL:** `https://api.reversecontact.com`
- **Official documentation:** [Fetch Post Comments](https://app.reversecontact.com/docs/endpoints/live-post-comments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityId` | body | `string` | yes | Social activity or post ID whose comments should be fetched. |
| `webhookUrl` | body | `string` | no | HTTPS callback URL for live results. |
