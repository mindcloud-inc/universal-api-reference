# boomApp Connect: Create Masked Two-Way SMS Thread

Creates a masked two-way SMS thread in boomApp Connect.

```
POST https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/create-masked-two-way-sms-thread
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a boomApp Connect `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/create-masked-two-way-sms-thread" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "from": "447890123456",
  "to": "447890123456",
  "reference": "reference-id",
  "message": "Initial message text"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boomAppConnect/latest/actions/create-masked-two-way-sms-thread', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "from": "447890123456",
    "to": "447890123456",
    "reference": "reference-id",
    "message": "Initial message text"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `from` | string | yes | Sender number for the masked two-way thread. Required for successful runtime submission. Example: `447890123456`. |
| `to` | string | yes | Recipient number for the masked two-way thread. Required for successful runtime submission. Example: `447890123456`. |
| `reference` | string | yes | Reference value for the masked two-way thread. Required for successful runtime submission. Example: `reference-id`. |
| `reference_always` | boolean | no | Whether the reference should always be included. |
| `rounds` | number | no | Number of conversation rounds. |
| `validity` | number | no | Thread validity period. |
| `message` | string | yes | Initial message for the masked two-way thread. Required for successful runtime submission. Example: `Initial message text`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": 1,
      "threadId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Response message. |
| `status` | number | Response status code. |
| `threadId` | number | Masked two-way SMS thread ID. |

## Native endpoint

Through the native boomApp Connect API, this operation is `POST /v1/maskTwoWay` (base URL `https://direct-api.apps.boomcomms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-masked-two-way-sms-thread.md) for the provider-specific parameters and requirements.

