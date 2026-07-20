# JetAPI: Get Delivery Status

Retrieves delivery status from JetAPI.

```
GET https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/get-delivery-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JetAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/get-delivery-status?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetAPI/latest/actions/get-delivery-status?${params}`, {
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
| `id` | number | yes | The JetAPI delivery identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "callbackUrl": "https://example.com",
      "externalId": "string",
      "id": 1,
      "operator": {},
      "phone": "string",
      "scheduledAt": "2026-05-07T12:00:00.000Z",
      "senderName": "Ava Chen",
      "simulateTyping": true,
      "status": {},
      "sum": "string",
      "totalSms": 1,
      "trafficCategory": 1,
      "utmMark": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callbackUrl` | string |  |
| `externalId` | string |  |
| `id` | number |  |
| `operator` | object |  |
| `phone` | string |  |
| `scheduledAt` | date |  |
| `senderName` | string |  |
| `simulateTyping` | boolean |  |
| `status` | object |  |
| `sum` | string |  |
| `totalSms` | number |  |
| `trafficCategory` | number |  |
| `utmMark` | string |  |

## Native endpoint

Through the native JetAPI API, this operation is `GET /api/v1/delivery/:id` (base URL `https://api.jetapi.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-delivery-status.md) for the provider-specific parameters and requirements.

