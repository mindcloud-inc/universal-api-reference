# Cin7 Core: Get Sale Fulfillment Pack



```
GET https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/get-sale-fulfillment-pack
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cin7 Core `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/get-sale-fulfillment-pack?connectionId=$CONNECTION_ID&TaskID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "TaskID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cin7core/latest/actions/get-sale-fulfillment-pack?${params}`, {
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
| `TaskID` | string | yes |  |
| `IncludeProductInfo` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "lines": [
        {
          "batchSN": {},
          "box": "string",
          "expiryDate": {},
          "location": "string",
          "locationID": "string",
          "name": "Ava Chen",
          "nonInventory": true,
          "productID": "string",
          "quantity": 1,
          "sku": "string",
          "warrantyRegistrationNumber": {}
        }
      ],
      "status": "string",
      "taskID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `lines[].batchSN` | object |  |
| `lines[].box` | string |  |
| `lines[].expiryDate` | object |  |
| `lines[].location` | string |  |
| `lines[].locationID` | string |  |
| `lines[].name` | string |  |
| `lines[].nonInventory` | boolean |  |
| `lines[].productID` | string |  |
| `lines[].quantity` | number |  |
| `lines[].sku` | string |  |
| `lines[].warrantyRegistrationNumber` | object |  |
| `status` | string |  |
| `taskID` | string |  |

## Native endpoint

Through the native Cin7 Core API, this operation is `GET sale/fulfilment/pack` (base URL `https://inventory.dearsystems.com/externalapi/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sale-fulfillment-pack.md) for the provider-specific parameters and requirements.

