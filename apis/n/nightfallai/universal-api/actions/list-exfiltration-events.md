# Nightfall.ai: List Exfiltration Events

Retrieves exfiltration events from Nightfall.ai.

```
GET https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/list-exfiltration-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nightfall.ai `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/list-exfiltration-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nightfallai/latest/actions/list-exfiltration-events?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<object> | Exfiltration events returned by Nightfall. |

## Native endpoint

Through the native Nightfall.ai API, this operation is `GET /exfiltration/v1/events` (base URL `https://api.nightfall.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-exfiltration-events.md) for the provider-specific parameters and requirements.

