# SigningHub: Fill Form Fields

Fills form fields in SigningHub.

```
PUT https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/fill-form-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SigningHub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/fill-form-fields" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "packageId": 1,
  "documentId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/signingHub/latest/actions/fill-form-fields', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "packageId": 1,
    "documentId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `packageId` | number | yes | The document package containing the form fields to fill. |
| `documentId` | number | yes | The document containing the form fields to fill. |
| `autoSave` | boolean | no | Whether to save the filled field values automatically. |
| `text[]` | array<object> | no | Text field values to fill, using objects with field_name and value. |
| `radio[]` | array<object> | no | Radio field values to fill, using objects supported by SigningHub. |
| `checkbox[]` | array<object> | no | Checkbox field values to fill, using objects supported by SigningHub. |
| `dropdown[]` | array<object> | no | Dropdown field values to fill, using objects supported by SigningHub. |
| `listbox[]` | array<object> | no | Listbox field values to fill, using objects supported by SigningHub. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native SigningHub API returns.

## Native endpoint

Through the native SigningHub API, this operation is `PUT /v4/packages/:packageId/documents/:documentId/fields` (base URL `https://api.signinghub.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fill-form-fields.md) for the provider-specific parameters and requirements.

