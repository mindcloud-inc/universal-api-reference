# Roborabbit: List Feeds

Retrieves custom task feeds from Roborabbit.

```
GET https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/list-feeds
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Roborabbit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/list-feeds?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/roborabbit/latest/actions/list-feeds?${params}`, {
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
      "description": "string",
      "lastRunAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "uid": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `lastRunAt` | date |  |
| `name` | string |  |
| `uid` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Roborabbit API, this operation is `GET /v1/feeds` (base URL `https://api.roborabbit.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-feeds.md) for the provider-specific parameters and requirements.

