# SEOTakeoff: Queue Article



```
POST https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/queue-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SEOTakeoff `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/queue-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "keyword": "string",
  "websiteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/queue-article', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "keyword": "string",
    "websiteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `keyword` | string | yes | Target SEO keyword for the queued article. |
| `websiteId` | string | yes | Website ID from List Websites. |
| `title` | string | no | Optional custom article title. |
| `clusterId` | string | no | Optional cluster ID to associate with the article. |
| `priority` | string | no | Optional priority: high, normal, or low. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "keyword": "string",
      "message": "string",
      "priority": "string",
      "queued_position": 1,
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `keyword` | string |  |
| `message` | string |  |
| `priority` | string |  |
| `queued_position` | number |  |
| `status` | string |  |
| `title` | string |  |

## Native endpoint

Through the native SEOTakeoff API, this operation is `POST /api/zapier/articles/queue` (base URL `https://api.seotakeoff.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/queue-article.md) for the provider-specific parameters and requirements.

