# FraudLabs Pro: Send SMS Verification

Sends an SMS verification in FraudLabs Pro.

```
POST https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/send-sms-verification
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FraudLabs Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/send-sms-verification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tel": "string",
  "mesg": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fraudLabsPro/latest/actions/send-sms-verification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tel": "string",
    "mesg": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tel` | string | yes | The recipient mobile phone number in E164 format. |
| `mesg` | string | yes | The SMS template including the <otp> placeholder. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "credits_remaining": 1,
      "tran_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_remaining` | number |  |
| `tran_id` | string |  |

## Native endpoint

Through the native FraudLabs Pro API, this operation is `POST v2/verification/send` (base URL `https://api.fraudlabspro.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms-verification.md) for the provider-specific parameters and requirements.

