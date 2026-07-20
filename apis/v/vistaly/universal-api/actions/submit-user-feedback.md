# Vistaly: Submit User Feedback

Creates user feedback in Vistaly.

```
POST https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/submit-user-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vistaly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/submit-user-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/submit-user-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | string | yes | The content of the feedback. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardIds[]` | array<string> | no | Optional card IDs to associate with this feedback. |
| `feedbackProviders[]` | array<object> | no | People who provided the feedback. |
| `feedbackReceivers[]` | array<object> | no | People who received the feedback. |
| `parseMarkdown` | boolean | no | Whether to parse the body as markdown. |
| `timestamp` | date | no | When the feedback was captured. |
| `url` | string | no | The URL where the feedback came from. |

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

Through the native Vistaly API, this operation is `POST /v1/feedback` (base URL `https://api.vistaly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-user-feedback.md) for the provider-specific parameters and requirements.

