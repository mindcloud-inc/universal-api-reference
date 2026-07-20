# Eventbrite: List Event Orders

Retrieves event orders from Eventbrite.

```
GET https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-event-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eventbrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-event-orders?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eventbrite/latest/actions/list-event-orders?${params}`, {
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
| `eventId` | string | yes | Event identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "changed": "string",
      "costs": {
        "basePrice": {
          "currency": "string",
          "display": "string",
          "majorValue": "string",
          "value": 1
        },
        "eventbriteFee": {
          "currency": "string",
          "display": "string",
          "majorValue": "string",
          "value": 1
        },
        "gross": {
          "currency": "string",
          "display": "string",
          "majorValue": "string",
          "value": 1
        },
        "hasGtsTax": true,
        "paymentFee": {
          "currency": "string",
          "display": "string",
          "majorValue": "string",
          "value": 1
        },
        "tax": {
          "currency": "string",
          "display": "string",
          "majorValue": "string",
          "value": 1
        }
      },
      "created": "string",
      "email": "ava@example.com",
      "eventId": "string",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "name": "Ava Chen",
      "resourceUri": "string",
      "status": "string",
      "timeRemaining": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `changed` | string |  |
| `costs.basePrice.currency` | string |  |
| `costs.basePrice.display` | string |  |
| `costs.basePrice.majorValue` | string |  |
| `costs.basePrice.value` | number |  |
| `costs.eventbriteFee.currency` | string |  |
| `costs.eventbriteFee.display` | string |  |
| `costs.eventbriteFee.majorValue` | string |  |
| `costs.eventbriteFee.value` | number |  |
| `costs.gross.currency` | string |  |
| `costs.gross.display` | string |  |
| `costs.gross.majorValue` | string |  |
| `costs.gross.value` | number |  |
| `costs.hasGtsTax` | boolean |  |
| `costs.paymentFee.currency` | string |  |
| `costs.paymentFee.display` | string |  |
| `costs.paymentFee.majorValue` | string |  |
| `costs.paymentFee.value` | number |  |
| `costs.tax.currency` | string |  |
| `costs.tax.display` | string |  |
| `costs.tax.majorValue` | string |  |
| `costs.tax.value` | number |  |
| `created` | string |  |
| `email` | string |  |
| `eventId` | string |  |
| `firstName` | string |  |
| `id` | string |  |
| `lastName` | string |  |
| `name` | string |  |
| `resourceUri` | string |  |
| `status` | string |  |
| `timeRemaining` | object |  |

## Native endpoint

Through the native Eventbrite API, this operation is `GET /events/:eventId/orders/` (base URL `https://www.eventbriteapi.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-event-orders.md) for the provider-specific parameters and requirements.

