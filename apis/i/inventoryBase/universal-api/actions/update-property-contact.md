# InventoryBase: Update Property Contact

Updates an existing property contact in InventoryBase.

```
PUT https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/update-property-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/update-property-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "deliver": true,
  "email": "ava@example.com",
  "name": "Ava Chen",
  "notify": true,
  "phone": "string",
  "propertyId": 1,
  "signee": true,
  "type": 1,
  "contactId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/update-property-contact', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "deliver": true,
    "email": "ava@example.com",
    "name": "Ava Chen",
    "notify": true,
    "phone": "string",
    "propertyId": 1,
    "signee": true,
    "type": 1,
    "contactId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `deliver` | boolean | yes | Whether to deliver to the contact |
| `email` | string | yes | Contact email |
| `name` | string | yes | Contact name |
| `notify` | boolean | yes | Whether to notify the contact |
| `phone` | string | yes | Contact phone |
| `propertyId` | number | yes | The InventoryBase property ID. |
| `signee` | boolean | yes | Whether the contact is a signee |
| `type` | number | yes | Contact type ID |
| `contactId` | number | yes | The InventoryBase contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deliver": true,
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "notify": true,
      "occupyOn": "string",
      "otherLabel": "string",
      "pending": true,
      "phone": "string",
      "reference": "string",
      "signee": true,
      "sms": true,
      "syncId": 1,
      "type": 1,
      "vacateOn": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deliver` | boolean |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `notify` | boolean |  |
| `occupyOn` | string |  |
| `otherLabel` | string |  |
| `pending` | boolean |  |
| `phone` | string |  |
| `reference` | string |  |
| `signee` | boolean |  |
| `sms` | boolean |  |
| `syncId` | number |  |
| `type` | number |  |
| `vacateOn` | string |  |

## Native endpoint

Through the native InventoryBase API, this operation is `PUT /properties/:propertyId/contacts/:contactId` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-property-contact.md) for the provider-specific parameters and requirements.

