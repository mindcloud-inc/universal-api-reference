# Podscan: List Topic Episodes

Retrieves episodes for a topic from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-topic-episodes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-topic-episodes?connectionId=$CONNECTION_ID&topicId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "topicId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/list-topic-episodes?${params}`, {
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
| `topicId` | string | yes | The topic ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "episodes": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `episodes` | array<object> |  |
| `pagination` | object |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /topics/{topicId}/episodes` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-topic-episodes.md) for the provider-specific parameters and requirements.

