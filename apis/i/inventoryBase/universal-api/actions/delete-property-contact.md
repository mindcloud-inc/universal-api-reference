# InventoryBase: Delete Property Contact

Deletes an existing property contact from InventoryBase.

```
DELETE https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/delete-property-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/delete-property-contact?connectionId=$CONNECTION_ID&propertyId=1&contactId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyId": "1",
  "contactId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/delete-property-contact?${params}`, {
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
| `propertyId` | number | yes | The InventoryBase property ID. |
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

Through the native InventoryBase API, this operation is `DELETE /properties/:propertyId/contacts/:contactId` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-property-contact.md) for the provider-specific parameters and requirements.

