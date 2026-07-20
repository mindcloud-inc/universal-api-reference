# Inoreader: Add Feed

Adds a new feed subscription in Inoreader.

```
POST https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/add-feed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Inoreader `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/add-feed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inoreader/latest/actions/add-feed', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedUrl` | string | yes | Feed URL to follow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "numResults": 1,
      "query": "string",
      "streamId": "string",
      "streamName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `numResults` | number | Number of matching feeds returned by quickadd. |
| `query` | string | The feed URL or query submitted to quickadd. |
| `streamId` | string | Canonical Inoreader stream ID for the created subscription. |
| `streamName` | string | Human-readable title of the resulting stream. |

## Native endpoint

Through the native Inoreader API, this operation is `POST /subscription/quickadd` (base URL `https://www.inoreader.com/reader/api/0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-feed.md) for the provider-specific parameters and requirements.

