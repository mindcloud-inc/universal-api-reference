# WebCategorize: Add URL Feedback



```
POST https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/add-url-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebCategorize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/add-url-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urlId": "https://example.com",
  "score": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/add-url-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urlId": "https://example.com",
    "score": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `urlId` | string | yes | The ID of the URL submission. |
| `score` | number | yes | Feedback score: 1 for positive feedback, 2 for negative feedback. |
| `language` | string | no | Language that should have been detected. |
| `classification[]` | array<string> | no | Category IDs that should have been detected. |
| `comment` | string | no | Optional feedback comment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the feedback request succeeded. |

## Native endpoint

Through the native WebCategorize API, this operation is `POST /url/feedback/{urlId}` (base URL `https://app.webcategorize.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-url-feedback.md) for the provider-specific parameters and requirements.

