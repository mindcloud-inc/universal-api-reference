# Sendblue: Send Typing Indicator

Sends an iMessage typing indicator through Sendblue.

```
POST https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/send-typing-indicator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/send-typing-indicator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "number": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/send-typing-indicator', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "number": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `number` | string | yes | The recipient phone number in E.164 format. |
| `fromNumber` | string | no | Your Sendblue line number in E.164 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errorMessage": {},
      "number": "string",
      "status": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errorMessage` | object |  |
| `number` | string |  |
| `status` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native Sendblue API, this operation is `POST /api/send-typing-indicator` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-typing-indicator.md) for the provider-specific parameters and requirements.

