# JetAPI: Create Bulk Delivery

Creates a new bulk delivery in JetAPI.

```
POST https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/create-bulk-delivery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JetAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/create-bulk-delivery" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "Bulk message",
  "phonesNumbers[]": "995598464533"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/create-bulk-delivery', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "Bulk message",
    "phonesNumbers[]": "995598464533"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes | Message text. Example: `Bulk message`. |
| `phonesNumbers[]` | array<string> | yes | Recipient phone numbers in international format. Example: `995598464533`. |
| `senderName` | string | no | Example: `InfoSMS`. |
| `scheduledAt` | date | no | UTC datetime in YYYY-MM-DD HH:MM:SS. Example: `2026-04-01 12:00:00`. |
| `utmMark` | string | no | Example: `campaign_mark`. |
| `dispatchRouting[]` | array<string> | no | Example: `whatsapp`. |
| `usernames[]` | array<string> | no | Example: `@username`. |
| `tdlibUserId` | string | no | Example: `-100123456`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dispatchRouting": [
        "string"
      ],
      "phonesNumbers": [
        "string"
      ],
      "scheduledAt": "2026-05-07T12:00:00.000Z",
      "senderName": "Ava Chen",
      "state": 1,
      "text": "string",
      "urlShorting": true,
      "utmMark": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dispatchRouting` | array<string> |  |
| `phonesNumbers` | array<string> |  |
| `scheduledAt` | date |  |
| `senderName` | string |  |
| `state` | number |  |
| `text` | string |  |
| `urlShorting` | boolean |  |
| `utmMark` | string |  |

## Native endpoint

Through the native JetAPI API, this operation is `POST /api/v1/bulk_delivery` (base URL `https://api.jetapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-bulk-delivery.md) for the provider-specific parameters and requirements.

