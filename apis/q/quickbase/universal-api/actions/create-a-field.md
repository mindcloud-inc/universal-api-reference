# Quickbase: Create a Field

Creates a new field in Quickbase.

```
POST https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/create-a-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quickbase `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/create-a-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": "string",
  "label": "string",
  "fieldType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/create-a-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": "string",
    "label": "string",
    "fieldType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableId` | string | yes | The Quickbase table identifier. |
| `label` | string | yes | The field label. |
| `fieldType` | string | yes | The Quickbase field type to create. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldHelp` | string | no | Optional help text for the field. |

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

Through the native Quickbase API, this operation is `POST v1/fields` (base URL `https://api.quickbase.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-field.md) for the provider-specific parameters and requirements.

