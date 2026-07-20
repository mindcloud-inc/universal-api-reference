# QDS: List Reviews



```
GET https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QDS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-reviews?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/qDS/latest/actions/list-reviews?${params}`, {
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
      "reviews": [
        {
          "approved_review": true,
          "comment": "string",
          "id": 1,
          "qa_comment": "string",
          "response_date": "2026-05-07T12:00:00.000Z",
          "score": 1,
          "service_date": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reviews[].approved_review` | boolean |  |
| `reviews[].comment` | string |  |
| `reviews[].id` | number |  |
| `reviews[].qa_comment` | string |  |
| `reviews[].response_date` | date |  |
| `reviews[].score` | number |  |
| `reviews[].service_date` | date |  |

## Native endpoint

Through the native QDS API, this operation is `GET /reviews` (base URL `https://qdsapp.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-reviews.md) for the provider-specific parameters and requirements.

