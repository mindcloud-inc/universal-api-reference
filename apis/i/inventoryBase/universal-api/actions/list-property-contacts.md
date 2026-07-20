# InventoryBase: List Property Contacts

Retrieves all contacts for a property in InventoryBase.

```
GET https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/list-property-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/list-property-contacts?connectionId=$CONNECTION_ID&propertyId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "propertyId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/list-property-contacts?${params}`, {
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

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native InventoryBase API returns.

## Native endpoint

Through the native InventoryBase API, this operation is `GET /properties/:propertyId/contacts` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-property-contacts.md) for the provider-specific parameters and requirements.

