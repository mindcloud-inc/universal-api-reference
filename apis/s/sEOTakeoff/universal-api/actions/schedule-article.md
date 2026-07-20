# SEOTakeoff: Schedule Article



```
PUT https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/schedule-article
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SEOTakeoff `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/schedule-article" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "articleId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sEOTakeoff/latest/actions/schedule-article', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "articleId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `articleId` | string | yes | Article ID from Generate Article or Search Articles. |
| `scheduledDate` | string | no | Optional ISO date to publish the article. |
| `scheduledTime` | string | no | Optional 24-hour time like 09:00. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "article_id": "string",
      "message": "string",
      "scheduled_for": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `article_id` | string |  |
| `message` | string |  |
| `scheduled_for` | string |  |
| `title` | string |  |

## Native endpoint

Through the native SEOTakeoff API, this operation is `POST /api/zapier/articles/schedule` (base URL `https://api.seotakeoff.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/schedule-article.md) for the provider-specific parameters and requirements.

