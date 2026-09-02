# Jetbuilt: Get Project Items



```
GET https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-project-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jetbuilt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-project-items?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jetbuilt/latest/actions/get-project-items?${params}`, {
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
| `projectId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bundle` | object |  |
| `cost` | string |  |
| `createdAt` | string |  |
| `currencyIso` | string |  |
| `custom` | boolean |  |
| `custom?` | boolean |  |
| `customProductId` | object |  |
| `discount` | string |  |
| `engineeringReleased` | boolean |  |
| `externalNotes` | string |  |
| `hidden` | boolean |  |
| `id` | number |  |
| `kind` | string |  |
| `laborPreset` | object |  |
| `manufacturerId` | number |  |
| `manufacturerName` | string |  |
| `mapp` | object |  |
| `model` | string |  |
| `msrp` | object |  |
| `msrpDiscountPercent` | object |  |
| `notes` | object |  |
| `option` | object |  |
| `ownerFurnished` | boolean |  |
| `partNumber` | object |  |
| `phase` | object |  |
| `price` | string |  |
| `productId` | number |  |
| `purchasingReleased` | boolean |  |
| `purchasingSource` | object |  |
| `quantity` | string |  |
| `quantityPerBundle` | object |  |
| `quantityPerRoom` | string |  |
| `room.id` | number |  |
| `room.name` | string |  |
| `room.quantity` | number |  |
| `selectedPurchasingVendor` | object |  |
| `shippingPrice` | string |  |
| `shortDescription` | string |  |
| `subcontractLaborCost` | string |  |
| `subcontractLaborPrice` | string |  |
| `subtotalEquipmentPrice` | string |  |
| `system.id` | number |  |
| `system.name` | string |  |
| `tag` | object |  |
| `taxEquipment` | boolean |  |
| `taxShipping` | boolean |  |
| `totalEquipmentPrice` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Jetbuilt API, this operation is `GET projects/:projectId/items` (base URL `https://app.jetbuilt.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-project-items.md) for the provider-specific parameters and requirements.

