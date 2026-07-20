# Podscan: Get Episode Engagement

Retrieves episode engagement details from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-episode-engagement
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-episode-engagement?connectionId=$CONNECTION_ID&episode=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "episode": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-episode-engagement?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `episode` | string | yes | The episode ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "engagement_data": {},
      "episode_id": "string",
      "episode_title": "string",
      "podcast_id": "string",
      "podcast_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `engagement_data` | object |  |
| `episode_id` | string |  |
| `episode_title` | string |  |
| `podcast_id` | string |  |
| `podcast_name` | string |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /episodes/{episode}/engagement` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-episode-engagement.md) for the provider-specific parameters and requirements.

