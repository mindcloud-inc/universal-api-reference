# ChipBot: List Articles



```
GET https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/list-articles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChipBot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/list-articles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chipBot/latest/actions/list-articles?${params}`, {
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
      "data": [
        {
          "analytics": {
            "impressions": 1,
            "rating": 1,
            "ratingCounter": 1,
            "ratingNegative": 1,
            "ratingPositive": 1,
            "views": 1
          },
          "contents": "string",
          "createdAt": "2026-05-07T12:00:00.000Z",
          "draft": true,
          "id": "string",
          "title": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "status": "string",
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Article rows. |
| `data[].analytics` | object | Article analytics. |
| `data[].analytics.impressions` | number | Impression count. |
| `data[].analytics.rating` | number | Average rating value. |
| `data[].analytics.ratingCounter` | number | Rating count. |
| `data[].analytics.ratingNegative` | number | Negative ratings. |
| `data[].analytics.ratingPositive` | number | Positive ratings. |
| `data[].analytics.views` | number | View count. |
| `data[].contents` | string | Rendered article contents. |
| `data[].createdAt` | date | Creation timestamp. |
| `data[].draft` | boolean | Draft status. |
| `data[].id` | string | Article identifier. |
| `data[].title` | string | Article title. |
| `data[].updatedAt` | date | Last update timestamp. |
| `status` | string | Provider response status. |
| `timestamp` | date | Provider timestamp. |

## Native endpoint

Through the native ChipBot API, this operation is `GET /api/v1/connect/accounts/:accountId/domains/:domainId/insights` (base URL `https://getchipbot.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-articles.md) for the provider-specific parameters and requirements.

