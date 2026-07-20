# Goldbelly: List Orders



```
GET https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/list-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goldbelly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/list-orders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goldbelly/latest/actions/list-orders?${params}`, {
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
| `shipDate` | date | no | Filters orders to ship on this date. Defaults to today when no date filter is provided. Example: 2019-11-15. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deliveryDate` | date | no | Filters by requested delivery date. Example: 2019-11-15. |
| `orderDate` | date | no | Filters by order completion date. Example: 2019-11-15. |
| `maxDaysInTransit` | number | no | Filters orders by the product's max days in transit. |
| `updatedAtOrAfter` | date | no | Filters orders updated at or after this time, or with line items updated at or after this time. Example: 2019-11-15T10:30:00Z. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedAt": "2026-05-07T12:00:00.000Z",
      "customerInstructionUrl": "https://example.com",
      "customerReferenceNumber": 1,
      "deliveryDate": "2026-05-07T12:00:00.000Z",
      "discountAmountInCents": 1,
      "discountCode": "string",
      "giftMessage": {
        "message": "string",
        "senderName": "Ava Chen"
      },
      "grFacility": true,
      "maxDaysInTransit": 1,
      "merchantStatus": "string",
      "orderId": 1,
      "products": [
        {
          "name": "Ava Chen",
          "quantity": 1,
          "sku": "string",
          "subproducts": [
            {
              "additionalInfo": "string",
              "name": "Ava Chen",
              "quantity": 1,
              "sku": "string"
            }
          ],
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "purchaserEmail": "ava@example.com",
      "purchaserName": "Ava Chen",
      "purchaserPhone": "string",
      "qrCodeImageUrl": "https://example.com",
      "shipDate": "2026-05-07T12:00:00.000Z",
      "shipper": {
        "id": 1,
        "name": "Ava Chen"
      },
      "shipping": {
        "carrier": "string",
        "packingSlipUrl": "https://example.com",
        "service": "string",
        "trackingNumber": "string"
      },
      "shippingAddress": {
        "city": "string",
        "company": "string",
        "country": "string",
        "firstName": "Ava",
        "lastName": "Chen",
        "postalCode": "string",
        "state": "string",
        "street1": "string",
        "street2": "string"
      },
      "shippingFacility": {
        "id": 1,
        "name": "Ava Chen",
        "shorthand": "string"
      },
      "shippingInCents": 1,
      "source": "string",
      "status": "string",
      "subtotalInCents": 1,
      "taxInCents": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "vip": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedAt` | date |  |
| `customerInstructionUrl` | string |  |
| `customerReferenceNumber` | number |  |
| `deliveryDate` | date |  |
| `discountAmountInCents` | number |  |
| `discountCode` | string |  |
| `giftMessage.message` | string |  |
| `giftMessage.senderName` | string |  |
| `grFacility` | boolean |  |
| `maxDaysInTransit` | number |  |
| `merchantStatus` | string |  |
| `orderId` | number |  |
| `products[].name` | string |  |
| `products[].quantity` | number |  |
| `products[].sku` | string |  |
| `products[].subproducts[].additionalInfo` | string |  |
| `products[].subproducts[].name` | string |  |
| `products[].subproducts[].quantity` | number |  |
| `products[].subproducts[].sku` | string |  |
| `products[].updatedAt` | date |  |
| `purchaserEmail` | string |  |
| `purchaserName` | string |  |
| `purchaserPhone` | string |  |
| `qrCodeImageUrl` | string |  |
| `shipDate` | date |  |
| `shipper.id` | number |  |
| `shipper.name` | string |  |
| `shipping.carrier` | string |  |
| `shipping.packingSlipUrl` | string |  |
| `shipping.service` | string |  |
| `shipping.trackingNumber` | string |  |
| `shippingAddress.city` | string |  |
| `shippingAddress.company` | string |  |
| `shippingAddress.country` | string |  |
| `shippingAddress.firstName` | string |  |
| `shippingAddress.lastName` | string |  |
| `shippingAddress.postalCode` | string |  |
| `shippingAddress.state` | string |  |
| `shippingAddress.street1` | string |  |
| `shippingAddress.street2` | string |  |
| `shippingFacility.id` | number |  |
| `shippingFacility.name` | string |  |
| `shippingFacility.shorthand` | string |  |
| `shippingInCents` | number |  |
| `source` | string |  |
| `status` | string |  |
| `subtotalInCents` | number |  |
| `taxInCents` | number |  |
| `updatedAt` | date |  |
| `vip` | boolean |  |

## Native endpoint

Through the native Goldbelly API, this operation is `GET orders` (base URL `https://api.goldbelly.com/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-orders.md) for the provider-specific parameters and requirements.

