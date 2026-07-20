# Podscan: Get Podcast Chart History

Retrieves podcast chart history from Podscan.

```
GET https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-podcast-chart-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Podscan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-podcast-chart-history?connectionId=$CONNECTION_ID&podcast=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "podcast": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/podscan/latest/actions/get-podcast-chart-history?${params}`, {
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
| `podcast` | string | yes | The podcast ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "chart_history": [
        {}
      ],
      "days_used": 1,
      "podcast_id": "string",
      "podcast_name": "Ava Chen",
      "trends": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chart_history` | array<object> |  |
| `days_used` | number |  |
| `podcast_id` | string |  |
| `podcast_name` | string |  |
| `trends` | object |  |

## Native endpoint

Through the native Podscan API, this operation is `GET /podcasts/{podcast}/chart-history` (base URL `https://podscan.fm/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-podcast-chart-history.md) for the provider-specific parameters and requirements.

