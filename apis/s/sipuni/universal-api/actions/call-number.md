# Sipuni: Call Number



```
POST https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/call-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sipuni `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/call-number" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "phone": "string",
  "sipnumber": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sipuni/latest/actions/call-number', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "phone": "string",
    "sipnumber": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `phone` | string | yes | External customer phone number to call. |
| `sipnumber` | string | yes | Sipuni employee short extension that initiates or receives the callback order. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reverse` | string | no | Sipuni callback mode flag. Default 0 follows the standard employee-to-customer callback order. Default: `0`. |
| `antiaon` | string | no | Caller ID hiding flag. Default 0 leaves caller ID behavior unchanged. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Raw response returned by Sipuni after submitting a call order. |

## Native endpoint

Through the native Sipuni API, this operation is `POST /callback/call_number` (base URL `https://sipuni.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/call-number.md) for the provider-specific parameters and requirements.

