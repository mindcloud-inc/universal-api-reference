# Jetbuilt: Get a Room

Retrieve the details of an individual project room. Equipment and labor totals (cost & price). Line items in this room. Project factors, along with how much of each factor applies to the room.

```
GET https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-a-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-a-room?connectionId=$CONNECTION_ID&projectId=1&roomId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "1",
  "roomId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-a-room?${params}`, {
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
| `projectId` | number | yes |  |
| `roomId` | string | yes | The Id of the Room to retrieve details for. To get a room ID, use the "Get All Rooms" Action to find the RoomId 's available for a given project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "equipmentTotalCost": {
        "cents": 1,
        "currencyIso": "string"
      },
      "equipmentTotalPrice": {
        "cents": 1,
        "currencyIso": "string"
      },
      "id": 1,
      "laborTotalCost": "string",
      "laborTotalPrice": "string",
      "lineItems": [
        {
          "bundle": {},
          "cost": "string",
          "createdAt": "string",
          "currencyIso": "string",
          "custom": true,
          "custom?": true,
          "customProductId": {},
          "discount": "string",
          "engineeringReleased": true,
          "externalNotes": "string",
          "hidden": true,
          "id": 1,
          "kind": "string",
          "laborPreset": {},
          "manufacturerId": 1,
          "manufacturerName": "Ava Chen",
          "mapp": {},
          "model": "string",
          "msrp": {},
          "msrpDiscountPercent": {},
          "notes": {},
          "option": {},
          "ownerFurnished": true,
          "partNumber": {},
          "phase": {},
          "price": "string",
          "productId": 1,
          "purchasingReleased": true,
          "purchasingSource": {},
          "quantity": "string",
          "quantityPerBundle": {},
          "quantityPerRoom": "string",
          "room": {
            "id": 1,
            "name": "Ava Chen",
            "quantity": 1
          },
          "selectedPurchasingVendor": {},
          "shippingPrice": "string",
          "shortDescription": "string",
          "subcontractLaborCost": "string",
          "subcontractLaborPrice": "string",
          "subtotalEquipmentPrice": "string",
          "system": {
            "id": 1,
            "name": "Ava Chen"
          },
          "tag": {},
          "taxEquipment": true,
          "taxShipping": true,
          "totalEquipmentPrice": "string",
          "updatedAt": "string"
        }
      ],
      "name": "Ava Chen",
      "otherTotalCost": {
        "cents": 1,
        "currencyIso": "string"
      },
      "otherTotalPrice": {
        "cents": 1,
        "currencyIso": "string"
      },
      "quantity": 1,
      "totalCost": {
        "cents": 1,
        "currencyIso": "string"
      },
      "totalPrice": {
        "cents": 1,
        "currencyIso": "string"
      },
      "totalTax": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `equipmentTotalCost.cents` | number |  |
| `equipmentTotalCost.currencyIso` | string |  |
| `equipmentTotalPrice.cents` | number |  |
| `equipmentTotalPrice.currencyIso` | string |  |
| `id` | number |  |
| `laborTotalCost` | string |  |
| `laborTotalPrice` | string |  |
| `lineItems[].bundle` | object |  |
| `lineItems[].cost` | string |  |
| `lineItems[].createdAt` | string |  |
| `lineItems[].currencyIso` | string |  |
| `lineItems[].custom` | boolean |  |
| `lineItems[].custom?` | boolean |  |
| `lineItems[].customProductId` | object |  |
| `lineItems[].discount` | string |  |
| `lineItems[].engineeringReleased` | boolean |  |
| `lineItems[].externalNotes` | string |  |
| `lineItems[].hidden` | boolean |  |
| `lineItems[].id` | number |  |
| `lineItems[].kind` | string |  |
| `lineItems[].laborPreset` | object |  |
| `lineItems[].manufacturerId` | number |  |
| `lineItems[].manufacturerName` | string |  |
| `lineItems[].mapp` | object |  |
| `lineItems[].model` | string |  |
| `lineItems[].msrp` | object |  |
| `lineItems[].msrpDiscountPercent` | object |  |
| `lineItems[].notes` | object |  |
| `lineItems[].option` | object |  |
| `lineItems[].ownerFurnished` | boolean |  |
| `lineItems[].partNumber` | object |  |
| `lineItems[].phase` | object |  |
| `lineItems[].price` | string |  |
| `lineItems[].productId` | number |  |
| `lineItems[].purchasingReleased` | boolean |  |
| `lineItems[].purchasingSource` | object |  |
| `lineItems[].quantity` | string |  |
| `lineItems[].quantityPerBundle` | object |  |
| `lineItems[].quantityPerRoom` | string |  |
| `lineItems[].room.id` | number |  |
| `lineItems[].room.name` | string |  |
| `lineItems[].room.quantity` | number |  |
| `lineItems[].selectedPurchasingVendor` | object |  |
| `lineItems[].shippingPrice` | string |  |
| `lineItems[].shortDescription` | string |  |
| `lineItems[].subcontractLaborCost` | string |  |
| `lineItems[].subcontractLaborPrice` | string |  |
| `lineItems[].subtotalEquipmentPrice` | string |  |
| `lineItems[].system.id` | number |  |
| `lineItems[].system.name` | string |  |
| `lineItems[].tag` | object |  |
| `lineItems[].taxEquipment` | boolean |  |
| `lineItems[].taxShipping` | boolean |  |
| `lineItems[].totalEquipmentPrice` | string |  |
| `lineItems[].updatedAt` | string |  |
| `name` | string |  |
| `otherTotalCost.cents` | number |  |
| `otherTotalCost.currencyIso` | string |  |
| `otherTotalPrice.cents` | number |  |
| `otherTotalPrice.currencyIso` | string |  |
| `quantity` | number |  |
| `totalCost.cents` | number |  |
| `totalCost.currencyIso` | string |  |
| `totalPrice.cents` | number |  |
| `totalPrice.currencyIso` | string |  |
| `totalTax` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Jetbuilt API, this operation is `GET projects/:projectId/rooms/:roomId` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-a-room.md) for the provider-specific parameters and requirements.

