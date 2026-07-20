# Helpjuice: List Article Analytics

Retrieves article analytics from Helpjuice.

```
GET https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/list-article-analytics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Helpjuice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/list-article-analytics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/list-article-analytics?${params}`, {
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
      "meta": {},
      "questions": [
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
| `meta` | object | Pagination metadata for the article analytics collection. |
| `questions` | array<object> | Per-article analytics rows returned by Helpjuice. |

## Native endpoint

Through the native Helpjuice API, this operation is `GET /analytics/questions` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-article-analytics.md) for the provider-specific parameters and requirements.

