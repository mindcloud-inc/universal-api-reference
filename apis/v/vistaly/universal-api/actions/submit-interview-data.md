# Vistaly: Submit Interview Data

Creates interview data in Vistaly.

```
POST https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/submit-interview-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vistaly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/submit-interview-data" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vistaly/latest/actions/submit-interview-data', {
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
| `body` | string | yes | The interview notepad content. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardIds[]` | array<string> | no | Optional card IDs to associate with this interview. |
| `feedbackProviders[]` | array<object> | no | People who provided the interview. |
| `feedbackReceivers[]` | array<object> | no | People who conducted the interview. |
| `parseMarkdown` | boolean | no | Whether to parse the body as markdown. |
| `timestamp` | date | no | When the interview was captured. |
| `url` | string | no | The URL where the interview came from. |

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

Through the native Vistaly API, this operation is `POST /v1/interviews` (base URL `https://api.vistaly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-interview-data.md) for the provider-specific parameters and requirements.

