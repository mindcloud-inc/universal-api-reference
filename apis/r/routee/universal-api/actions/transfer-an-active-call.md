# Routee: Transfer an active call

Transfers an active call in Routee.

```
PUT https://connect.mindcloud.co/v1/universal/routee/latest/actions/transfer-an-active-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/routee/latest/actions/transfer-an-active-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageId": "string",
  "from": "string",
  "to": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/transfer-an-active-call', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageId": "string",
    "from": "string",
    "to": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageId` | string | yes | The id of the voice call to be transfered. |
| `from` | string | yes | The sender Id for this call |
| `to` | object | yes | The recipient of the call |
| `hangupDelay` | number | no | The time to wait for the call to be answered. |
| `maxDuration` | number | no | Defines the maximum duration. |
| `callback` | object | no | Defines the notification callback information for the progress of the Voice call. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "message": "string",
      "messageId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `message` | string |  |
| `messageId` | string |  |

## Native endpoint

Through the native Routee API, this operation is `POST /voice/conversation/:messageId/transfer` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transfer-an-active-call.md) for the provider-specific parameters and requirements.

