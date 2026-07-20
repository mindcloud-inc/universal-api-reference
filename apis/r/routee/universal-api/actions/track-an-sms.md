# Routee: Track an SMS

Tracks an SMS message in Routee.

```
GET https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-an-sms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Routee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-an-sms?connectionId=$CONNECTION_ID&trackingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/routee/latest/actions/track-an-sms?${params}`, {
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
| `trackingId` | string | yes | The unique tracking id of the sms |

## Response

```json
{
  "success": true,
  "data": [
    {
      "applicationName": "Ava Chen",
      "body": "string",
      "country": "string",
      "direction": "string",
      "from": "string",
      "groups": [
        [
          "string"
        ]
      ],
      "latency": 1,
      "messageId": "string",
      "operator": "string",
      "originatingService": "string",
      "part": 1,
      "parts": 1,
      "price": 1,
      "smsId": "string",
      "status": {
        "date": "string",
        "reason": {
          "description": "string",
          "detailedStatus": "string"
        },
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
| `body` | string |  |
| `country` | string |  |
| `direction` | string |  |
| `from` | string |  |
| `groups[]` | array |  |
| `latency` | number |  |
| `messageId` | string |  |
| `operator` | string |  |
| `originatingService` | string |  |
| `part` | number |  |
| `parts` | number |  |
| `price` | number |  |
| `smsId` | string |  |
| `status` | object |  |
| `status.date` | string |  |
| `status.reason` | object |  |
| `status.reason.description` | string |  |
| `status.reason.detailedStatus` | string |  |
| `status.status` | string |  |
| `to` | string |  |

## Native endpoint

Through the native Routee API, this operation is `GET /sms/tracking/single/:trackingId` (base URL `https://connect.routee.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/track-an-sms.md) for the provider-specific parameters and requirements.

