# Fraser Direct: Get purchase order information



```
GET https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/get-purchase-order-information
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fraser Direct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/get-purchase-order-information?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/get-purchase-order-information?${params}`, {
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
| `depositorOrderNumber` | string | no | Provide DepositorOrderNumber, ShipmentIdentificationNumber, or both. |
| `shipmentIdentificationNumber` | string | no | Provide DepositorOrderNumber, ShipmentIdentificationNumber, or both. If both are provided, they must match the same purchase order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "depositorOrderNumber": "string",
      "detailList": [
        {}
      ],
      "detailReceivedList": [
        {}
      ],
      "errorList": [
        {}
      ],
      "fraserRef": "string",
      "poDate": "string",
      "priority": "string",
      "receivedDate": "string",
      "shipmentIdentificationNumber": "string",
      "status": "string",
      "success": "string",
      "totalReceivedQuantity": 1,
      "vendorNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `depositorOrderNumber` | string |  |
| `detailList` | array<object> |  |
| `detailReceivedList` | array<object> |  |
| `errorList` | array<object> |  |
| `fraserRef` | string |  |
| `poDate` | string |  |
| `priority` | string |  |
| `receivedDate` | string |  |
| `shipmentIdentificationNumber` | string |  |
| `status` | string |  |
| `success` | string |  |
| `totalReceivedQuantity` | number |  |
| `vendorNumber` | string |  |

## Native endpoint

Through the native Fraser Direct API, this operation is `GET /GetPOInformation` (base URL `https://apiv2test.fraserdirect.ca/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-purchase-order-information.md) for the provider-specific parameters and requirements.

