# WhatsBoost: Send USSD Request

Sends a USSD request from WhatsBoost.

```
POST https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/send-ussd-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WhatsBoost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/send-ussd-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "code": "string",
  "sim": 1,
  "device": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/whatsBoost/latest/actions/send-ussd-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "code": "string",
    "sim": 1,
    "device": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `code` | string | yes | MMI request code. Please make sure that you are using a valid MMI code, if not, it will fail. |
| `sim` | number | yes | SIM slot number you want to use. |
| `device` | string | yes | Linked device unique ID. You can get linked device unique ID from /get/devices (Your devices). |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native WhatsBoost API, this operation is `POST /send/ussd` (base URL `https://whatsboost.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-ussd-request.md) for the provider-specific parameters and requirements.

