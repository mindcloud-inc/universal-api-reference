# InsightIQ: Create Async Content Comments Fetch

Creates an async content comments fetch request in InsightIQ.

```
POST https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/create-async-content-comments-fetch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InsightIQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/create-async-content-comments-fetch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contentUrl": "https://example.com",
  "workPlatformId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/insightIQ/latest/actions/create-async-content-comments-fetch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contentUrl": "https://example.com",
    "workPlatformId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contentUrl` | string | yes | Public content URL to fetch comments for |
| `maxResult` | number | no | Maximum number of comments to fetch Default: `100`. |
| `workPlatformId` | string | yes | Work platform ID for the content source |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content_url": "https://example.com",
      "id": "string",
      "max_results": 1,
      "work_platform": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content_url` | string |  |
| `id` | string |  |
| `max_results` | number |  |
| `work_platform` | object |  |

## Native endpoint

Through the native InsightIQ API, this operation is `POST /v1/social/creators/async/contents/comments/fetch` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-async-content-comments-fetch.md) for the provider-specific parameters and requirements.

