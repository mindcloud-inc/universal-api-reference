# Fetch Post Details with Reverse Contact

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/fetch/post/live`
- **Base URL:** `https://api.reversecontact.com`
- **Official documentation:** [Fetch Post Details](https://app.reversecontact.com/docs/endpoints/live-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `activityId` | body | `string` | yes | Social activity or post ID to fetch live. |
| `webhookUrl` | body | `string` | no | HTTPS callback URL for live results. |
