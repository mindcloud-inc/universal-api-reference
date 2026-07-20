# UserBit: List Insights

Retrieves insights from a UserBit repository project.

```
GET https://connect.mindcloud.co/v1/universal/userBit/latest/actions/list-insights
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserBit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userBit/latest/actions/list-insights?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userBit/latest/actions/list-insights?${params}`, {
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
      "createdBy": "string",
      "htmlContent": "string",
      "id": "string",
      "imageUrl": "https://example.com",
      "priority": "string",
      "textContent": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string | Insight author name. |
| `htmlContent` | string | Insight HTML content. |
| `id` | string | Insight identifier. |
| `imageUrl` | string | Insight image URL. |
| `priority` | string | Insight priority label. |
| `textContent` | string | Insight plain-text content. |
| `title` | string | Insight title. |

## Native endpoint

Through the native UserBit API, this operation is `GET /v1/insights/list` (base URL `https://userbit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-insights.md) for the provider-specific parameters and requirements.

