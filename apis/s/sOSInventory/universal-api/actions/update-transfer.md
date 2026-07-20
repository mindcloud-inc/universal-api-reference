# SOS Inventory: Update Transfer

Updates an existing transfer in SOS Inventory.

```
PUT https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SOS Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "number": "string",
  "date": "string",
  "fromLocation.name": "Ava Chen",
  "toLocation.name": "Ava Chen",
  "lines[].item.name": "Ava Chen",
  "lines[].quantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sOSInventory/latest/actions/update-transfer', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "number": "string",
    "date": "string",
    "fromLocation.name": "Ava Chen",
    "toLocation.name": "Ava Chen",
    "lines[].item.name": "Ava Chen",
    "lines[].quantity": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `number` | string | yes |  |
| `date` | string | yes |  |
| `fromLocation.name` | string | yes |  |
| `toLocation.name` | string | yes |  |
| `comment` | string | no |  |
| `lines[].item.name` | string | yes |  |
| `lines[].quantity` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "comment": "string",
      "createBillForShippingAmount": true,
      "customFields": {},
      "date": "string",
      "department": {},
      "fromLocation": {
        "id": 1,
        "name": "Ava Chen"
      },
      "hasSignature": true,
      "id": 1,
      "keys": {},
      "lines": [
        {
          "class": {},
          "description": "string",
          "fromBin": {},
          "id": 1,
          "item": {
            "id": 1,
            "name": "Ava Chen"
          },
          "job": {},
          "lineNumber": 1,
          "lot": {},
          "quantity": 1,
          "toBin": {},
          "uom": {},
          "volume": 1,
          "volumeunit": "string",
          "weight": 1,
          "weightunit": "string",
          "workcenter": {}
        }
      ],
      "number": "string",
      "shippingAmount": 1,
      "shippingMethod": {},
      "starred": 1,
      "summaryOnly": true,
      "syncToken": 1,
      "toLocation": {
        "id": 1,
        "name": "Ava Chen"
      },
      "total": 1,
      "trackingNumber": "string",
      "values": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `comment` | string |  |
| `createBillForShippingAmount` | boolean |  |
| `customFields` | object |  |
| `date` | string |  |
| `department` | object |  |
| `fromLocation.id` | number |  |
| `fromLocation.name` | string |  |
| `hasSignature` | boolean |  |
| `id` | number |  |
| `keys` | object |  |
| `lines[].class` | object |  |
| `lines[].description` | string |  |
| `lines[].fromBin` | object |  |
| `lines[].id` | number |  |
| `lines[].item.id` | number |  |
| `lines[].item.name` | string |  |
| `lines[].job` | object |  |
| `lines[].lineNumber` | number |  |
| `lines[].lot` | object |  |
| `lines[].quantity` | number |  |
| `lines[].toBin` | object |  |
| `lines[].uom` | object |  |
| `lines[].volume` | number |  |
| `lines[].volumeunit` | string |  |
| `lines[].weight` | number |  |
| `lines[].weightunit` | string |  |
| `lines[].workcenter` | object |  |
| `number` | string |  |
| `shippingAmount` | number |  |
| `shippingMethod` | object |  |
| `starred` | number |  |
| `summaryOnly` | boolean |  |
| `syncToken` | number |  |
| `toLocation.id` | number |  |
| `toLocation.name` | string |  |
| `total` | number |  |
| `trackingNumber` | string |  |
| `values` | object |  |

## Native endpoint

Through the native SOS Inventory API, this operation is `PUT /api/v2/transfer/:id` (base URL `https://api.sosinventory.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-transfer.md) for the provider-specific parameters and requirements.

