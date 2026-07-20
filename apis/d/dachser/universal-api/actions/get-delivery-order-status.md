# Dachser: Get Delivery Order Status

Retrieves delivery order status from Dachser.

```
GET https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-delivery-order-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dachser `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-delivery-order-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-delivery-order-status?${params}`, {
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
| `purchaseOrderNumber` | string | no | Purchase order number. |
| `referenceNumber1` | string | no | First delivery order reference number. |
| `referenceNumber2` | string | no | Second delivery order reference number. |
| `referenceNumber3` | string | no | Third delivery order reference number. |
| `deliveryOrderDate` | date | no | Delivery order date. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventCode` | string | no | Warehouse order status event code. |
| `customerId` | string | no | Optional customer ID. |
| `acceptLanguage` | string | no | Optional language sent as the Accept-Language header. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "consignee": {},
      "deliveryDate": "2026-05-07T12:00:00.000Z",
      "deliveryOrders": [
        {}
      ],
      "id": "string",
      "orderDate": "2026-05-07T12:00:00.000Z",
      "principal": {},
      "references": {},
      "status": [
        {}
      ],
      "warehouse": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `consignee` | object |  |
| `deliveryDate` | date |  |
| `deliveryOrders` | array<object> |  |
| `id` | string |  |
| `orderDate` | date |  |
| `principal` | object |  |
| `references` | object |  |
| `status` | array<object> |  |
| `warehouse` | object |  |

## Native endpoint

Through the native Dachser API, this operation is `GET /rest/v2/deliveryorderstatus` (base URL `https://api-gateway.dachser.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-delivery-order-status.md) for the provider-specific parameters and requirements.

