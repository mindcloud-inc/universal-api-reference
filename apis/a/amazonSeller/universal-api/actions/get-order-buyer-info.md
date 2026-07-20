# Amazon Seller: Get Order Buyer Info

Retrieves buyer information for an Amazon Seller order.

```
GET https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-order-buyer-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Amazon Seller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-order-buyer-info?connectionId=$CONNECTION_ID&orderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/amazonSeller/latest/actions/get-order-buyer-info?${params}`, {
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
| `orderId` | string | yes | The Amazon order identifier in 3-7-7 format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amazonOrderId": "string",
      "buyerName": "Ava Chen",
      "buyerTaxInfo": {
        "companyLegalName": "Ava Chen"
      },
      "purchaseOrderNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amazonOrderId` | string |  |
| `buyerName` | string |  |
| `buyerTaxInfo.companyLegalName` | string |  |
| `purchaseOrderNumber` | string |  |

## Native endpoint

Through the native Amazon Seller API, this operation is `GET orders/v0/orders/:orderId/buyerInfo` (base URL `https://{{credentials.environment}}-{{credentials.region}}.amazon.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-buyer-info.md) for the provider-specific parameters and requirements.

