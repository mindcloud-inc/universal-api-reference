# InventoryBase: Update Property

Updates an existing property record in InventoryBase.

```
PUT https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/update-property
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/update-property" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "propertyId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/update-property', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "propertyId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `propertyId` | number | yes | The InventoryBase property ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native InventoryBase API returns.

## Native endpoint

Through the native InventoryBase API, this operation is `PUT /properties/:propertyId` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-property.md) for the provider-specific parameters and requirements.

