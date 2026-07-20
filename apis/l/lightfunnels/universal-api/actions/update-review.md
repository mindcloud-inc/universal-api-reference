# Lightfunnels: Update Review



```
PUT https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/update-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lightfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/update-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lightfunnels/latest/actions/update-review', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "updateReview": {
        "id": "string",
        "name": "Ava Chen",
        "published": true,
        "rate": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `updateReview` | object | Updated review. |
| `updateReview.id` | string | Review id. |
| `updateReview.name` | string | Reviewer name. |
| `updateReview.published` | boolean | Whether the review is published. |
| `updateReview.rate` | number | Review rating. |

## Native endpoint

Through the native Lightfunnels API, this operation is `POST /api/v2` (base URL `https://services.lightfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-review.md) for the provider-specific parameters and requirements.

