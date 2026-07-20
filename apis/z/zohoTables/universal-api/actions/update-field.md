# Zoho Tables: Update Field

Updates an existing field in Zoho Tables.

```
PUT https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/update-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Tables `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/update-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "baseId": "string",
  "tableId": "string",
  "fieldId": "string",
  "type": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoTables/latest/actions/update-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "baseId": "string",
    "tableId": "string",
    "fieldId": "string",
    "type": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `baseId` | string | yes |  |
| `tableId` | string | yes |  |
| `fieldId` | string | yes |  |
| `fieldName` | string | no |  |
| `type` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultValue": "string",
      "fieldId": "string",
      "name": "Ava Chen",
      "type": "string",
      "typeComponents": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultValue` | string | Field default value when present. |
| `fieldId` | string | Zoho field identifier. |
| `name` | string | Field name. |
| `type` | string | Zoho field type code. |
| `typeComponents` | object | Type-specific field settings. |

## Native endpoint

Through the native Zoho Tables API, this operation is `PUT /fields` (base URL `https://tables.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-field.md) for the provider-specific parameters and requirements.

