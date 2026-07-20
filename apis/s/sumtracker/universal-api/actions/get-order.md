# Sumtracker: Get Purchase Order or Stock Transfer

Retrieves a purchase order or stock transfer from Sumtracker.

```
GET https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/get-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/get-order?connectionId=$CONNECTION_ID&document_type=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "document_type": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/get-order?${params}`, {
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
| `document_type` | string | yes | Use `orders` for purchase orders or `stock-transfers` for stock transfers. |
| `id` | string | yes | Purchase order or stock transfer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "number": "string",
      "billingAddress": {
        "companyName": "Ava Chen",
        "firstName": "Ava",
        "lastName": "Chen",
        "email": "ava@example.com",
        "phone": "string",
        "addressLine1": "string",
        "addressLine2": "string",
        "city": "string",
        "state": "string",
        "pincode": "string",
        "country": "string",
        "taxNum": "string",
        "id": 1
      },
      "shippingAddress": {
        "companyName": "Ava Chen",
        "firstName": "Ava",
        "lastName": "Chen",
        "email": "ava@example.com",
        "phone": "string",
        "addressLine1": "string",
        "addressLine2": "string",
        "city": "string",
        "state": "string",
        "pincode": "string",
        "country": "string",
        "taxNum": "string",
        "id": 1
      },
      "reference": "string",
      "status": 1,
      "actionPerformed": "string",
      "isTaskInProgress": true,
      "currency": "string",
      "shipByTime": "2026-05-07T12:00:00.000Z",
      "created": "2026-05-07T12:00:00.000Z",
      "updated": "2026-05-07T12:00:00.000Z",
      "totalQuantity": 1,
      "totalAmount": "string",
      "subtotal": "string",
      "totalTax": "string",
      "totalShipping": "string",
      "extraCharges": "string",
      "extraShipping": "string",
      "conversionRate": "string",
      "notes": "string",
      "paymentTerms": "string",
      "shippingCarrier": "string",
      "trackingNumber": "string",
      "trackingUrl": "https://example.com",
      "id": 1,
      "contactId": 1,
      "warehouseId": 1,
      "fromWarehouseId": {},
      "billingAddressId": 1,
      "shippingAddressId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `number` | string |  |
| `billingAddress.companyName` | string |  |
| `billingAddress.firstName` | string |  |
| `shippingAddress.companyName` | string |  |
| `billingAddress.lastName` | string |  |
| `shippingAddress.firstName` | string |  |
| `shippingAddress.lastName` | string |  |
| `reference` | string |  |
| `billingAddress.email` | string |  |
| `billingAddress.phone` | string |  |
| `shippingAddress.email` | string |  |
| `shippingAddress.phone` | string |  |
| `status` | number |  |
| `actionPerformed` | string |  |
| `isTaskInProgress` | boolean |  |
| `currency` | string |  |
| `shipByTime` | date |  |
| `created` | date |  |
| `updated` | date |  |
| `totalQuantity` | number |  |
| `totalAmount` | string |  |
| `subtotal` | string |  |
| `totalTax` | string |  |
| `totalShipping` | string |  |
| `extraCharges` | string |  |
| `extraShipping` | string |  |
| `conversionRate` | string |  |
| `billingAddress.addressLine1` | string |  |
| `billingAddress.addressLine2` | string |  |
| `shippingAddress.addressLine1` | string |  |
| `billingAddress.city` | string |  |
| `shippingAddress.addressLine2` | string |  |
| `billingAddress.state` | string |  |
| `shippingAddress.city` | string |  |
| `billingAddress.pincode` | string |  |
| `shippingAddress.state` | string |  |
| `billingAddress.country` | string |  |
| `shippingAddress.pincode` | string |  |
| `shippingAddress.country` | string |  |
| `notes` | string |  |
| `paymentTerms` | string |  |
| `shippingCarrier` | string |  |
| `trackingNumber` | string |  |
| `trackingUrl` | string |  |
| `billingAddress.taxNum` | string |  |
| `shippingAddress.taxNum` | string |  |
| `id` | number |  |
| `contactId` | number |  |
| `warehouseId` | number |  |
| `fromWarehouseId` | object |  |
| `billingAddressId` | number |  |
| `shippingAddressId` | number |  |
| `billingAddress.id` | number |  |
| `shippingAddress.id` | number |  |

## Native endpoint

Through the native Sumtracker API, this operation is `GET /api/version/2025-03/purchases/:document_type/:id/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order.md) for the provider-specific parameters and requirements.

