# Pinch Payments: Get Event

Retrieves an event from Pinch Payments.

```
GET https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinch Payments `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/get-event?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/get-event?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "eventId": "string",
        "payer": {
          "id": "string"
        }
      },
      "eventDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "merchantId": "string",
      "metadata": {
        "merchantName": "Ava Chen",
        "merchantStatus": "string",
        "payerName": "Ava Chen",
        "status": "string",
        "submissionDateUtc": "2026-05-07T12:00:00.000Z"
      },
      "type": "string",
      "webhooks": [
        {
          "id": "string",
          "requestEndUtc": "2026-05-07T12:00:00.000Z",
          "requestStartUtc": "2026-05-07T12:00:00.000Z",
          "responseCode": 1,
          "webhookId": "string",
          "webhookUri": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.eventId` | string |  |
| `data.payer.id` | string |  |
| `eventDate` | date |  |
| `id` | string |  |
| `merchantId` | string |  |
| `metadata.merchantName` | string |  |
| `metadata.merchantStatus` | string |  |
| `metadata.payerName` | string |  |
| `metadata.status` | string |  |
| `metadata.submissionDateUtc` | date |  |
| `type` | string |  |
| `webhooks[].id` | string |  |
| `webhooks[].requestEndUtc` | date |  |
| `webhooks[].requestStartUtc` | date |  |
| `webhooks[].responseCode` | number |  |
| `webhooks[].webhookId` | string |  |
| `webhooks[].webhookUri` | string |  |

## Native endpoint

Through the native Pinch Payments API, this operation is `GET /events/[:id]` (base URL `https://api.getpinch.com.au/live`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

