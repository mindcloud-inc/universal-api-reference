# InventoryBase: Create Inspection

Creates a new inspection in InventoryBase.

```
POST https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/create-inspection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/create-inspection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "property": {},
  "type": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/create-inspection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "property": {},
    "type": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `property` | object | yes | Property object containing the property ID |
| `type` | object | yes | Inspection type object containing the type ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedAt": "string",
      "clerk": {
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen"
      },
      "createdAt": "string",
      "id": 1,
      "invoice": {
        "id": 1
      },
      "pricing": {
        "price": 1
      },
      "property": {
        "id": 1,
        "ref": "string"
      },
      "reportKey": "string",
      "state": {
        "id": 1,
        "name": "Ava Chen"
      },
      "type": {
        "id": 1,
        "name": "Ava Chen"
      },
      "updatedAt": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedAt` | string |  |
| `clerk` | object |  |
| `clerk.email` | string |  |
| `clerk.id` | number |  |
| `clerk.name` | string |  |
| `createdAt` | string |  |
| `id` | number |  |
| `invoice` | object |  |
| `invoice.id` | number |  |
| `pricing` | object |  |
| `pricing.price` | number |  |
| `property` | object |  |
| `property.id` | number |  |
| `property.ref` | string |  |
| `reportKey` | string |  |
| `state` | object |  |
| `state.id` | number |  |
| `state.name` | string |  |
| `type` | object |  |
| `type.id` | number |  |
| `type.name` | string |  |
| `updatedAt` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native InventoryBase API, this operation is `POST /inspections` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-inspection.md) for the provider-specific parameters and requirements.

