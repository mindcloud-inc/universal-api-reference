# SmartRoutes: Get Order



```
GET https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartRoutes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/get-order?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/get-order?${params}`, {
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
| `id` | number | yes | ID of the order to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attachments": [
        {}
      ],
      "capacities": [
        {}
      ],
      "created": "2026-05-07T12:00:00.000Z",
      "customer": {},
      "customFields": [
        {}
      ],
      "deliveryAddress": "string",
      "deliveryDate": "2026-05-07T12:00:00.000Z",
      "deliveryLat": 1,
      "deliveryLng": 1,
      "deliveryNotes": "string",
      "emails": [
        {}
      ],
      "lineItems": [
        {}
      ],
      "orderNumber": "string",
      "parts": 1,
      "priority": "string",
      "skills": [
        "string"
      ],
      "status": "string",
      "stops": [
        {}
      ],
      "tags": [
        "string"
      ],
      "thirdParty": {},
      "timeWindows": [
        {}
      ],
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attachments` | array<object> | Order attachments. |
| `capacities` | array<object> | Order capacities. |
| `created` | date | Order creation timestamp. |
| `customer` | object | Customer reference for the order. |
| `customFields` | array<object> | Order custom fields. |
| `deliveryAddress` | string | Delivery address. |
| `deliveryDate` | date | Delivery date. |
| `deliveryLat` | number | Delivery latitude. |
| `deliveryLng` | number | Delivery longitude. |
| `deliveryNotes` | string | Delivery notes. |
| `emails` | array<object> | Order email records. |
| `lineItems` | array<object> | Order line items. |
| `orderNumber` | string | SmartRoutes order number. |
| `parts` | number | Order part count. |
| `priority` | string | Order priority. |
| `skills` | array<string> | Order skills. |
| `status` | string | Order status. |
| `stops` | array<object> | Order stops. |
| `tags` | array<string> | Order tags. |
| `thirdParty` | object | Third-party handoff details. |
| `timeWindows` | array<object> | Order time windows. |
| `type` | string | Order type. |
| `updated` | date | Order last updated timestamp. |

## Native endpoint

Through the native SmartRoutes API, this operation is `GET /orders/:id` (base URL `https://api.smartroutes.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

