# SmartSuite: Update Field

Updates an existing field in SmartSuite.

```
PUT https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/update-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/update-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": "69b45da87cb40fc74dbb4b84",
  "slug": "mctestfld2",
  "label": "MC Test Field B Updated",
  "fieldType": "textfield",
  "params": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/update-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": "69b45da87cb40fc74dbb4b84",
    "slug": "mctestfld2",
    "label": "MC Test Field B Updated",
    "fieldType": "textfield",
    "params": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableId` | string | yes | The SmartSuite table ID containing the field to update. Example: `69b45da87cb40fc74dbb4b84`. |
| `slug` | string | yes | The SmartSuite field slug to update. Example: `mctestfld2`. |
| `label` | string | yes | The updated field label. Example: `MC Test Field B Updated`. |
| `fieldType` | string | yes | The SmartSuite field type to keep or change. Example: `textfield`. |
| `params` | object | yes | The field-specific params object. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SmartSuite API returns.

## Native endpoint

Through the native SmartSuite API, this operation is `PUT /applications/:tableId/change_field/` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-field.md) for the provider-specific parameters and requirements.

