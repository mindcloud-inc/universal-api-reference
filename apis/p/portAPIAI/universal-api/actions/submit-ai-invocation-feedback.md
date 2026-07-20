# Port API AI: Submit AI Invocation Feedback



```
PUT https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/submit-ai-invocation-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/submit-ai-invocation-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedbackRating": "string",
  "invocationIdentifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/submit-ai-invocation-feedback', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedbackRating": "string",
    "invocationIdentifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `comment` | string | no | Feedback comment. |
| `feedbackRating` | string | yes | Feedback rating. |
| `invocationIdentifier` | string | yes | The AI invocation identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Port API AI API, this operation is `PATCH /ai/invoke/:invocation_identifier/feedback` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-ai-invocation-feedback.md) for the provider-specific parameters and requirements.

