# Product Fruits: Create Feedback



```
POST https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/create-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Product Fruits `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/create-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string",
  "username": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/productFruits/latest/actions/create-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string",
    "username": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `environmentInfo.userAgent` | string | no | User agent string of the submitter device. |
| `text` | string | yes | Feedback text. |
| `username` | string | yes | Username of the user submitting feedback. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorName": "Ava Chen",
      "authorProps": "string",
      "authorUsername": "Ava Chen",
      "environmentInfo": "string",
      "id": 1,
      "isNative": true,
      "isSolved": true,
      "screenshots": [
        {}
      ],
      "sentAt": "2026-05-07T12:00:00.000Z",
      "text": "string",
      "videos": [
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
| `authorName` | string |  |
| `authorProps` | string |  |
| `authorUsername` | string |  |
| `environmentInfo` | string |  |
| `id` | number |  |
| `isNative` | boolean |  |
| `isSolved` | boolean |  |
| `screenshots` | array<object> |  |
| `sentAt` | date |  |
| `text` | string |  |
| `videos` | array<object> |  |

## Native endpoint

Through the native Product Fruits API, this operation is `POST /v1/feedback` (base URL `https://api.productfruits.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-feedback.md) for the provider-specific parameters and requirements.

