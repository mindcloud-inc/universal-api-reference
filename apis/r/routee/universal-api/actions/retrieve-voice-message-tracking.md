# Routee: Retrieve Voice Message Tracking

Retrieves voice message tracking from Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-voice-message-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-voice-message-tracking?connectionId=$CONNECTION_ID&messageTrackingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "messageTrackingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/retrieve-voice-message-tracking?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageTrackingId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationName": "Ava Chen",
      "campaign": "string",
      "chargeInterval": 1,
      "country": "string",
      "direction": "string",
      "duration": 1,
      "from": "string",
      "groups": [
        [
          "string"
        ]
      ],
      "message": {
        "gender": "string",
        "language": "string",
        "text": "string"
      },
      "messageId": "string",
      "originatingService": "string",
      "price": 1,
      "recordings": [
        [
          "string"
        ]
      ],
      "status": {
        "date": "string",
        "status": "string"
      },
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `applicationName` | string |  |
| `campaign` | string |  |
| `chargeInterval` | number |  |
| `country` | string |  |
| `direction` | string |  |
| `duration` | number |  |
| `from` | string |  |
| `groups[]` | array<string> |  |
| `message` | object |  |
| `message.gender` | string |  |
| `message.language` | string |  |
| `message.text` | string |  |
| `messageId` | string |  |
| `originatingService` | string |  |
| `price` | number |  |
| `recordings[]` | array |  |
| `status` | object |  |
| `status.date` | string |  |
| `status.status` | string |  |
| `to` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /voice/tracking/:messageTrackingId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-voice-message-tracking.md) for the provider-specific parameters and requirements.

