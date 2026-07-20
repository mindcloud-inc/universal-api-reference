# InventoryBase: Get Inspection

Retrieves an inspection from InventoryBase by ID.

```
GET https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-inspection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-inspection?connectionId=$CONNECTION_ID&inspectionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inspectionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-inspection?${params}`, {
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
| `inspectionId` | number | yes | The ID of the inspection |

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
      "notes": {},
      "pricing": {
        "price": 1
      },
      "property": {
        "address": {
          "city": "string",
          "line1": "string",
          "postcode": "string"
        },
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
| `notes` | object |  |
| `pricing` | object |  |
| `pricing.price` | number |  |
| `property` | object |  |
| `property.address` | object |  |
| `property.address.city` | string |  |
| `property.address.line1` | string |  |
| `property.address.postcode` | string |  |
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

Through the native InventoryBase API, this operation is `GET /inspections/:inspectionId` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inspection.md) for the provider-specific parameters and requirements.

