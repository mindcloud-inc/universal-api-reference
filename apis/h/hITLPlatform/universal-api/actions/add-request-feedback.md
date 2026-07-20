# HITL Platform: Add Request Feedback



```
POST https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/add-request-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HITL Platform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/add-request-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hITLPlatform/latest/actions/add-request-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedback.accuracy` | number | no | Accuracy rating from 1 to 5. |
| `feedback.category` | string | no | Feedback category such as positive, constructive, or issue. |
| `feedback.comment` | string | no | Free-form feedback comment. |
| `feedback.helpfulness` | number | no | Helpfulness rating from 1 to 5. |
| `feedback.rating` | number | no | Overall quality rating from 1 to 5. |
| `feedback.timeliness` | number | no | Timeliness rating from 1 to 5. |
| `feedback.wouldRecommend` | boolean | no | Whether you would recommend this reviewer for similar work. |
| `id` | string | yes | The unique identifier of the completed request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "feedback": {
        "accuracy": 1,
        "category": "string",
        "comment": "string",
        "helpfulness": 1,
        "rating": 1,
        "tags": [
          [
            "string"
          ]
        ],
        "timeliness": 1,
        "would_recommend": true
      },
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `feedback.accuracy` | number |  |
| `feedback.category` | string |  |
| `feedback.comment` | string |  |
| `feedback.helpfulness` | number |  |
| `feedback.rating` | number |  |
| `feedback.tags[]` | array<string> |  |
| `feedback.timeliness` | number |  |
| `feedback.would_recommend` | boolean |  |
| `request_id` | string |  |

## Native endpoint

Through the native HITL Platform API, this operation is `POST /api/requests/:id/feedback` (base URL `https://api.hitl.sh/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-request-feedback.md) for the provider-specific parameters and requirements.

