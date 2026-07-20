# Fraser Direct: Create order



```
POST https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fraser Direct `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stName": "Ava Chen",
  "stAddress1": "string",
  "stCity": "string",
  "stProvince": "string",
  "stPostalCode": "string",
  "stCountry": "string",
  "poDate": "2024-11-06",
  "serviceLevel": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stName": "Ava Chen",
    "stAddress1": "string",
    "stCity": "string",
    "stProvince": "string",
    "stPostalCode": "string",
    "stCountry": "string",
    "poDate": "2024-11-06",
    "serviceLevel": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderNumber` | string | no | Order number. OrderNumber or PO must be provided. |
| `po` | string | no | Purchase order number. OrderNumber or PO must be provided. |
| `stName` | string | yes | Required ship-to name. |
| `stAddress1` | string | yes | Required ship-to address line 1. |
| `stAddress2` | string | no | Optional ship-to address line 2. |
| `stCity` | string | yes | Required ship-to city. |
| `stProvince` | string | yes | Required 2-character ship-to province. |
| `stPostalCode` | string | yes | Required ship-to postal code. |
| `stCountry` | string | yes | Required 3-character country code. |
| `shipPhone` | string | no | Optional ship-to phone number. |
| `poDate` | string | yes | Required order date in YYYY-MM-DD format. Example: `2024-11-06`. |
| `requestedDeliveryDate` | string | no | Optional requested delivery date in YYYY-MM-DD format. Example: `2024-11-08`. |
| `warehouseInstructions` | string | no | Optional warehouse instructions. Fraser Direct's field name is spelled WarehouseIntructions in the API docs. |
| `carrier` | string | no | Optional carrier. If omitted, Fraser Direct rate shops based on ServiceLevel. |
| `serviceLevel` | string | yes | Required service level. Valid values are STANDARD or EXPRESS. |
| `detailList` | object<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "orderNumber": "string",
      "orderStatus": "string",
      "po": "string",
      "success": "string",
      "validationResults": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `orderNumber` | string |  |
| `orderStatus` | string |  |
| `po` | string |  |
| `success` | string |  |
| `validationResults` | array<object> |  |

## Native endpoint

Through the native Fraser Direct API, this operation is `POST /CreateOrder` (base URL `https://apiv2test.fraserdirect.ca/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

