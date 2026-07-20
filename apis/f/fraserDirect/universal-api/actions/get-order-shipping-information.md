# Fraser Direct: Get order shipping information



```
GET https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/get-order-shipping-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fraser Direct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/get-order-shipping-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/get-order-shipping-information?${params}`, {
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
| `orderNumber` | string | no | Provide OrderNumber, PO, or both. |
| `po` | string | no | Provide OrderNumber, PO, or both. If both are provided, they must match the same order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actualCarrier": "string",
      "actualSCAC": "string",
      "detailList": [
        {}
      ],
      "errorList": [
        {}
      ],
      "fraserRef": "string",
      "orderNumber": "string",
      "po": "string",
      "shipDate": "string",
      "status": "string",
      "success": "string",
      "totalCost": 1,
      "totalShippedCartons": 1,
      "totalShippedQuantity": 1,
      "totalShippedWeight": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actualCarrier` | string |  |
| `actualSCAC` | string |  |
| `detailList` | array<object> |  |
| `errorList` | array<object> |  |
| `fraserRef` | string |  |
| `orderNumber` | string |  |
| `po` | string |  |
| `shipDate` | string |  |
| `status` | string |  |
| `success` | string |  |
| `totalCost` | number |  |
| `totalShippedCartons` | number |  |
| `totalShippedQuantity` | number |  |
| `totalShippedWeight` | number |  |

## Native endpoint

Through the native Fraser Direct API, this operation is `GET /GetOrderShippingInformation` (base URL `https://apiv2test.fraserdirect.ca/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-shipping-information.md) for the provider-specific parameters and requirements.

