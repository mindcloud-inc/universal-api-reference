# Quickbase: Update a Field

Updates an existing field in Quickbase.

```
PUT https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/update-a-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quickbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/update-a-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": "string",
  "fieldId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/update-a-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": "string",
    "fieldId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableId` | string | yes | The Quickbase table identifier. |
| `fieldId` | number | yes | The Quickbase field identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `label` | string | no | Optional new field label. |
| `fieldHelp` | string | no | Optional new help text for the field. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "appearsByDefault": true,
      "audited": true,
      "fieldHelp": "string",
      "fieldType": "string",
      "findEnabled": true,
      "id": 1,
      "label": "string",
      "mode": "string",
      "permissions": [
        {}
      ],
      "properties": {},
      "required": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `appearsByDefault` | boolean | Whether the field appears by default. |
| `audited` | boolean | Whether the field is audited. |
| `fieldHelp` | string | The field help text. |
| `fieldType` | string | The Quickbase field type. |
| `findEnabled` | boolean | Whether the field is searchable. |
| `id` | number | The Quickbase field ID. |
| `label` | string | The field label. |
| `mode` | string | The field mode. |
| `permissions` | array<object> | Field permissions by role. |
| `properties` | object | Field-specific properties. |
| `required` | boolean | Whether the field is required. |

## Native endpoint

Through the native Quickbase API, this operation is `POST v1/fields/:fieldId` (base URL `https://api.quickbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-a-field.md) for the provider-specific parameters and requirements.

