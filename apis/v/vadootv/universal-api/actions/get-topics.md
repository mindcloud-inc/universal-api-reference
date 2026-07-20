# Vadootv: Get topics

Retrieves available video topics from Vadootv.

```
GET https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-topics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vadootv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-topics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vadootv/latest/actions/get-topics?${params}`, {
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
    {}
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `[]` | array<string> | Available video topic names. |

## Native endpoint

Through the native Vadootv API, this operation is `GET /api/get_topics` (base URL `https://aiapi.vadoo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-topics.md) for the provider-specific parameters and requirements.

