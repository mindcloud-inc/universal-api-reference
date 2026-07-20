# Reka AI: List Legacy Videos

Retrieves legacy videos from Reka AI.

```
GET https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/list-legacy-videos
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/list-legacy-videos?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/list-legacy-videos?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Primary identifier. |
| `name` | string | Display name. |
| `status` | string | Status value. |

## Native endpoint

Through the native Reka AI API, this operation is `GET https://vision-agent.api.reka.ai/v1/videos` (base URL `https://api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-legacy-videos.md) for the provider-specific parameters and requirements.

