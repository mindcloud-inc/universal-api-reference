# SmartSuite: Add Field

Creates a new field in SmartSuite.

```
POST https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/add-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/add-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": "69b45da87cb40fc74dbb4b84",
  "field": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/add-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": "69b45da87cb40fc74dbb4b84",
    "field": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableId` | string | yes | The SmartSuite table ID where the field should be created. Example: `69b45da87cb40fc74dbb4b84`. |
| `field` | object | yes | The SmartSuite field object to create, including slug, label, field_type, params, and is_new. Example: `[object Object]`. |
| `fieldPosition` | object | no | Optional SmartSuite field position object, such as prev_sibling_slug. Example: `[object Object]`. |
| `autoFillStructureLayout` | boolean | no | Whether SmartSuite should add the new field to the structure layout automatically. Default: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SmartSuite API returns.

## Native endpoint

Through the native SmartSuite API, this operation is `POST /applications/:tableId/add_field/` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-field.md) for the provider-specific parameters and requirements.

