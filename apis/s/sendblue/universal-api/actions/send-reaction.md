# Sendblue: Send Reaction

Sends an iMessage reaction through Sendblue.

```
POST https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/send-reaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendblue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/send-reaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fromNumber": "string",
  "messageHandle": "string",
  "reaction": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendblue/latest/actions/send-reaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fromNumber": "string",
    "messageHandle": "string",
    "reaction": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fromNumber` | string | yes | Your Sendblue line number in E.164 format. |
| `messageHandle` | string | yes | The inbound webhook message_handle value to react to. |
| `reaction` | string | yes | The tapback reaction to send. |
| `partIndex` | number | no | The zero-based part index for a multi-part message. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "messageHandle": "string",
      "reaction": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |
| `messageHandle` | string |  |
| `reaction` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Sendblue API, this operation is `POST /api/send-reaction` (base URL `https://api.sendblue.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-reaction.md) for the provider-specific parameters and requirements.

