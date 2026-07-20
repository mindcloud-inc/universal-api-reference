# SMS Connexion: Send SMS In Conversation

Sends an SMS reply in SMS Connexion.

```
POST https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/send-sms-in-conversation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMS Connexion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/send-sms-in-conversation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conversationId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sMSConnexion/latest/actions/send-sms-in-conversation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conversationId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conversationId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignId": "string",
      "cost": 1,
      "countryIso": "string",
      "createdAt": "string",
      "data": {},
      "dlrCallbackUrl": "https://example.com",
      "from": "string",
      "info": {},
      "length": 1,
      "msgId": "string",
      "parts": 1,
      "phoneNumbersByCountry": {},
      "scheduled": true,
      "status": "string",
      "text": "string",
      "textAnalysis": {},
      "to": "string",
      "totalCost": 1,
      "totalInvalid": 1,
      "totalParts": 1,
      "totalPhoneNumbers": 1,
      "totalValid": 1,
      "unicode": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignId` | string |  |
| `cost` | number |  |
| `countryIso` | string |  |
| `createdAt` | string |  |
| `data` | object |  |
| `dlrCallbackUrl` | string |  |
| `from` | string |  |
| `info` | object |  |
| `length` | number |  |
| `msgId` | string |  |
| `parts` | number |  |
| `phoneNumbersByCountry` | object |  |
| `scheduled` | boolean |  |
| `status` | string |  |
| `text` | string |  |
| `textAnalysis` | object |  |
| `to` | string |  |
| `totalCost` | number |  |
| `totalInvalid` | number |  |
| `totalParts` | number |  |
| `totalPhoneNumbers` | number |  |
| `totalValid` | number |  |
| `unicode` | boolean |  |

## Native endpoint

Through the native SMS Connexion API, this operation is `POST /conversations/:conversationId/sms` (base URL `https://api.sms.cx`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms-in-conversation.md) for the provider-specific parameters and requirements.

