# InventoryBase: Delete Inspection Contact

Deletes an existing inspection contact from InventoryBase.

```
DELETE https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/delete-inspection-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InventoryBase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/delete-inspection-contact?connectionId=$CONNECTION_ID&contactId=1&inspectionId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "1",
  "inspectionId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/delete-inspection-contact?${params}`, {
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
| `contactId` | number | yes | The ID of the contact |
| `inspectionId` | number | yes | The ID of the inspection |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native InventoryBase API returns.

## Native endpoint

Through the native InventoryBase API, this operation is `DELETE /inspections/:inspectionId/contacts/:contactId` (base URL `https://api.inventorybase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-inspection-contact.md) for the provider-specific parameters and requirements.

