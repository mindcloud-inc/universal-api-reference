# Pinch Payments: List Events

Retrieves events from Pinch Payments.

```
GET https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinch Payments `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/list-events?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinchPayments/latest/actions/list-events?${params}`, {
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
| `endDate` | date | no |  |
| `eventType` | string | no |  |
| `startDate` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "eventDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "metadata": {
        "merchantName": "Ava Chen",
        "merchantStatus": "string",
        "status": "string",
        "submissionDateUtc": "2026-05-07T12:00:00.000Z"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `eventDate` | date |  |
| `id` | string |  |
| `metadata.merchantName` | string |  |
| `metadata.merchantStatus` | string |  |
| `metadata.status` | string |  |
| `metadata.submissionDateUtc` | date |  |
| `type` | string |  |

## Native endpoint

Through the native Pinch Payments API, this operation is `GET /events` (base URL `https://api.getpinch.com.au/live`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

