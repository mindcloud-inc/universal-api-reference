# Chroma Vector Store: Heartbeat

Retrieves the current nanosecond timestamp from Chroma.

```
GET https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/heartbeat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chroma Vector Store `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/heartbeat?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chromaVectorStore/latest/actions/heartbeat?${params}`, {
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
      "nanosecond heartbeat": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nanosecond heartbeat` | number |  |

## Native endpoint

Through the native Chroma Vector Store API, this operation is `GET /api/v2/heartbeat` (base URL `https://api.trychroma.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/heartbeat.md) for the provider-specific parameters and requirements.

