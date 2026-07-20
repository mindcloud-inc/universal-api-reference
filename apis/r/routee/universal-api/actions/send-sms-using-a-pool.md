# Routee: Send SMS using a Pool

Sends SMS using a pool with Routee.

```
POST https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-sms-using-a-pool
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-sms-using-a-pool" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "poolId": "string",
  "to": "string",
  "poolStrategy": "string",
  "body": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/routee/latest/actions/send-sms-using-a-pool', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "poolId": "string",
    "to": "string",
    "poolStrategy": "string",
    "body": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `poolId` | string | yes | The tracking id of the pool. |
| `to` | string | yes | The recipient of the SMS. Format with a '+' and country code e.g., +3069485xxxxx (E.164 format). |
| `poolStrategy` | string | yes | The strategy to follow when picking a sender from the pool. Values: Numeric, Alphanumeric |
| `body` | string | yes | The body of the SMS message. |
| `urlShortener` | object | no | [OPTIONAL] If present, each link that exist in message body will be replaced by a Shortened URL. NOTE: Links are recognized by the prefix "http://" or "https://" and are separated by the next word or character with space. Keep in mind that adding any character like '.' ',' etc, other than space at the end of the link, will be recognized as part of the url and it will result to a shortened url that redirects to a wrong destination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "body": "string",
      "bodyAnalysis": {
        "characters": 1,
        "parts": 1,
        "unicode": true
      },
      "createdAt": "string",
      "from": "string",
      "poolId": "string",
      "poolName": "Ava Chen",
      "poolStrategy": "string",
      "smsSettings": {
        "alphanumericSenderId": "string",
        "geomatch": true,
        "sticky": true,
        "transcode": true
      },
      "status": "string",
      "to": "string",
      "trackingId": "string",
      "urlShortener": {
        "urls": [
          [
            {}
          ]
        ],
        "urlValidity": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `body` | string |  |
| `bodyAnalysis` | object |  |
| `bodyAnalysis.characters` | number |  |
| `bodyAnalysis.parts` | number |  |
| `bodyAnalysis.unicode` | boolean |  |
| `createdAt` | string |  |
| `from` | string |  |
| `poolId` | string |  |
| `poolName` | string |  |
| `poolStrategy` | string |  |
| `smsSettings` | object |  |
| `smsSettings.alphanumericSenderId` | string |  |
| `smsSettings.geomatch` | boolean |  |
| `smsSettings.sticky` | boolean |  |
| `smsSettings.transcode` | boolean |  |
| `status` | string |  |
| `to` | string |  |
| `trackingId` | string |  |
| `urlShortener` | object |  |
| `urlShortener.urls[]` | array<object> |  |
| `urlShortener.urls[].longUrl` | string |  |
| `urlShortener.urls[].shortUrl` | string |  |
| `urlShortener.urlValidity` | number |  |

## Native endpoint

Through the native Routee API, this operation is `POST /pools/my/:poolId/sms` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-sms-using-a-pool.md) for the provider-specific parameters and requirements.

