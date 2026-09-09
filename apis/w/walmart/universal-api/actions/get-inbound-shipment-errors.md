# Walmart: Get Inbound Shipment Errors

Retrieve a list of errors for an inbound shipment request.

```
GET https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-inbound-shipment-errors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Walmart `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-inbound-shipment-errors?connectionId=$CONNECTION_ID&limit=25&offset=0&inboundOrderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "inboundOrderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/walmart/latest/actions/get-inbound-shipment-errors?${params}`, {
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
| `inboundOrderId` | string | yes | Unique ID identifying inbound shipment request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDate": "string",
      "errors": [
        {
          "category": "string",
          "code": "string",
          "description": "string",
          "field": "string",
          "info": "string",
          "severity": "string"
        }
      ],
      "inboundOrderId": "string",
      "orderItems": [
        {
          "expectedDeliveryDate": "string",
          "innerPackQty": 1,
          "itemDesc": "string",
          "itemQty": 1,
          "productId": "string",
          "productType": "string",
          "sku": "string",
          "vendorPackQty": 1
        }
      ],
      "returnAddress": {
        "addressLine1": "string",
        "city": "string",
        "countryCode": "string",
        "postalCode": "string",
        "stateCode": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDate` | string |  |
| `errors[].category` | string |  |
| `errors[].code` | string |  |
| `errors[].description` | string |  |
| `errors[].field` | string |  |
| `errors[].info` | string |  |
| `errors[].severity` | string |  |
| `inboundOrderId` | string |  |
| `orderItems[].expectedDeliveryDate` | string |  |
| `orderItems[].innerPackQty` | number |  |
| `orderItems[].itemDesc` | string |  |
| `orderItems[].itemQty` | number |  |
| `orderItems[].productId` | string |  |
| `orderItems[].productType` | string |  |
| `orderItems[].sku` | string |  |
| `orderItems[].vendorPackQty` | number |  |
| `returnAddress.addressLine1` | string |  |
| `returnAddress.city` | string |  |
| `returnAddress.countryCode` | string |  |
| `returnAddress.postalCode` | string |  |
| `returnAddress.stateCode` | string |  |

## Native endpoint

Through the native Walmart API, this operation is `GET /v3/fulfillment/inbound-shipment-errors` (base URL `https://{{credentials.environment}}.walmartapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-inbound-shipment-errors.md) for the provider-specific parameters and requirements.

