# Queue: Get Service

Retrieves a service from Queue.

```
GET https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Queue `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-service?connectionId=$CONNECTION_ID&serviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "serviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/queue/latest/actions/get-service?${params}`, {
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
| `serviceId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "addon": true,
      "cancelAtPeriodEnd": true,
      "checkoutLink": "https://example.com",
      "couponId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultPrice": "string",
      "description": "string",
      "disablePause": true,
      "disableQuantity": true,
      "id": "string",
      "limitPausing": 1,
      "minimumMonths": 1,
      "position": 1,
      "previewImage": "string",
      "requirePaymentMethod": true,
      "servicePrices": [
        {}
      ],
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `addon` | boolean |  |
| `cancelAtPeriodEnd` | boolean |  |
| `checkoutLink` | string |  |
| `couponId` | string |  |
| `createdAt` | date |  |
| `defaultPrice` | string |  |
| `description` | string |  |
| `disablePause` | boolean |  |
| `disableQuantity` | boolean |  |
| `id` | string |  |
| `limitPausing` | number |  |
| `minimumMonths` | number |  |
| `position` | number |  |
| `previewImage` | string |  |
| `requirePaymentMethod` | boolean |  |
| `servicePrices` | array<object> |  |
| `title` | string |  |

## Native endpoint

Through the native Queue API, this operation is `GET services/:service_id` (base URL `https://app.usequeue.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-service.md) for the provider-specific parameters and requirements.

