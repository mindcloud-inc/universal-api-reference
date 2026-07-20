# Podscan: List Episode Entities

Retrieves entities mentioned in an episode from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-episode-entities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-episode-entities?connectionId=$CONNECTION_ID&episodeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "episodeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-episode-entities?${params}`, {
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
| `episodeId` | string | yes | The episode ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "entities": [
        {}
      ],
      "episode_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entities` | array<object> |  |
| `episode_id` | string |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /episodes/{episodeId}/entities` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-episode-entities.md) for the provider-specific parameters and requirements.

