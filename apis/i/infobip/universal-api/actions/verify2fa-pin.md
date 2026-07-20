# Infobip: Verify 2FA PIN



```
PUT https://connect.mindcloud.co/v1/universal/infobip/latest/actions/verify2fa-pin
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Infobip `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/infobip/latest/actions/verify2fa-pin" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pinId": "string",
  "pin": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infobip/latest/actions/verify2fa-pin', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pinId": "string",
    "pin": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pinId` | string | yes | ID of the pin code that has to be verified. |
| `pin` | string | yes | The PIN code to verify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attemptsRemaining": 1,
      "msisdn": "string",
      "pinError": "string",
      "pinId": "string",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attemptsRemaining` | number |  |
| `msisdn` | string |  |
| `pinError` | string |  |
| `pinId` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Infobip API, this operation is `POST /2fa/2/pin/{pinId}/verify` (base URL `https://rkpzwe.api.infobip.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify2fa-pin.md) for the provider-specific parameters and requirements.

