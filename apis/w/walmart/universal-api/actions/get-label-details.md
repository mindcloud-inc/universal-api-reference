# Walmart: Get Label Details

Retrieves all label details generated for a purchase order id.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-label-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-label-details?connectionId=$CONNECTION_ID&purchaseOrderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "purchaseOrderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-label-details?${params}`, {
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
| `purchaseOrderId` | string | yes | A unique `purchaseOrderId` to retrieve label details for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addOns": [
        {
          "charge": {
            "amount": 1,
            "currency": "string"
          },
          "declaredValue": {
            "amount": 1,
            "currency": "string"
          },
          "name": "Ava Chen",
          "refLink": "https://example.com",
          "status": "string"
        }
      ],
      "boxItems": [
        {
          "lineNumber": "string",
          "quantity": 1,
          "sku": "string"
        }
      ],
      "carrierFullName": "Ava Chen",
      "carrierName": "Ava Chen",
      "carrierServiceType": "string",
      "purchaseOrderId": "string",
      "trackingNo": "string",
      "trackingUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addOns[].charge.amount` | number |  |
| `addOns[].charge.currency` | string |  |
| `addOns[].declaredValue.amount` | number |  |
| `addOns[].declaredValue.currency` | string |  |
| `addOns[].name` | string |  |
| `addOns[].refLink` | string |  |
| `addOns[].status` | string |  |
| `boxItems[].lineNumber` | string |  |
| `boxItems[].quantity` | number |  |
| `boxItems[].sku` | string |  |
| `carrierFullName` | string |  |
| `carrierName` | string |  |
| `carrierServiceType` | string |  |
| `purchaseOrderId` | string |  |
| `trackingNo` | string |  |
| `trackingUrl` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/shipping/labels/purchase-orders/:purchaseOrderId` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-label-details.md) for the provider-specific parameters and requirements.

