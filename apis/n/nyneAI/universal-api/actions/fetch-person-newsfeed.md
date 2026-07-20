# Nyne AI: Fetch Person Newsfeed

Retrieves social media posts for a person from Nyne AI.

```
GET https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/fetch-person-newsfeed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nyne AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/fetch-person-newsfeed?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nyneAI/latest/actions/fetch-person-newsfeed?${params}`, {
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
      "message": "string",
      "posts": [
        {}
      ],
      "request_id": "string",
      "results": [
        {}
      ],
      "status": "string",
      "success": true,
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `posts` | array<object> |  |
| `request_id` | string |  |
| `results` | array<object> |  |
| `status` | string |  |
| `success` | boolean |  |
| `timestamp` | date |  |

## Native endpoint

Through the native Nyne AI API, this operation is `POST /person/newsfeed` (base URL `https://api.nyne.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-person-newsfeed.md) for the provider-specific parameters and requirements.

