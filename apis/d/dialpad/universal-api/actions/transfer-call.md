# Dialpad: Transfer Call

Transfers a call to another recipient in Dialpad.

```
PUT https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/transfer-call
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/transfer-call" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/transfer-call', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The call's id. |
| `to` | object | no | Destination of the call transfer. |
| `transfer_state` | string | no | The state which the call should take when it's transferred. |
| `custom_data` | string | no | Extra data to associate with the call. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callId": "string",
      "transferredToNumber": "string",
      "transferredToState": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callId` | string | The call ID. |
| `transferredToNumber` | string | The phone number the call was transferred to. |
| `transferredToState` | string | The state the call was transferred to. |

## Native endpoint

Through the native Dialpad API, this operation is `POST /call/:id/transfer` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/transfer-call.md) for the provider-specific parameters and requirements.

