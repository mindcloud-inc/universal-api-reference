# Gumroad: Get Subscriber

Retrieves a subscriber from Gumroad.

```
GET https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gumroad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-subscriber?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gumroad/latest/actions/get-subscriber?${params}`, {
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
| `id` | string | yes | The subscriber ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "subscribers": {
        "cancelledAt": "2026-05-07T12:00:00.000Z",
        "chargeOccurrenceCount": 1,
        "createdAt": "2026-05-07T12:00:00.000Z",
        "endedAt": "2026-05-07T12:00:00.000Z",
        "failedAt": "2026-05-07T12:00:00.000Z",
        "freeTrialEndsAt": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "licenseKey": "string",
        "productId": "string",
        "productName": "Ava Chen",
        "purchaseIds": [
          [
            "string"
          ]
        ],
        "recurrence": "string",
        "status": "string",
        "userEmail": "ava@example.com",
        "userId": "string",
        "userRequestedCancellationAt": "2026-05-07T12:00:00.000Z"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `subscribers` | object |  |
| `subscribers.cancelledAt` | date |  |
| `subscribers.chargeOccurrenceCount` | number |  |
| `subscribers.createdAt` | date |  |
| `subscribers.endedAt` | date |  |
| `subscribers.failedAt` | date |  |
| `subscribers.freeTrialEndsAt` | date |  |
| `subscribers.id` | string |  |
| `subscribers.licenseKey` | string |  |
| `subscribers.productId` | string |  |
| `subscribers.productName` | string |  |
| `subscribers.purchaseIds[]` | array<string> |  |
| `subscribers.recurrence` | string |  |
| `subscribers.status` | string |  |
| `subscribers.userEmail` | string |  |
| `subscribers.userId` | string |  |
| `subscribers.userRequestedCancellationAt` | date |  |
| `success` | boolean |  |

## Native endpoint

Through the native Gumroad API, this operation is `GET /subscribers/:id` (base URL `https://api.gumroad.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscriber.md) for the provider-specific parameters and requirements.

