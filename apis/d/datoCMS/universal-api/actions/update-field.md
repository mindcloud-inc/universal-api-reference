# DatoCMS: Update Field



```
PUT https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fieldId": "string",
  "attributes": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-field', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fieldId": "string",
    "attributes": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fieldId` | string | yes | Field ID. |
| `attributes` | object | yes | Field attributes payload. Example: `[object Object]`. |
| `attributes.defaultValue` | object | no |  |
| `attributes.label` | string | no |  |
| `attributes.apiKey` | string | no |  |
| `attributes.localized` | boolean | no |  |
| `attributes.validators` | object | no |  |
| `attributes.appeareance` | object | no |  |
| `attributes.appearance` | object | no |  |
| `attributes.position` | number | no |  |
| `attributes.fieldType` | string | no |  |
| `attributes.hint` | string | no |  |
| `attributes.deepFilteringEnabled` | boolean | no |  |
| `attributes.defaultValue.en` | string | no |  |
| `attributes.defaultValue.it` | string | no |  |
| `attributes.validators.required` | object | no |  |
| `attributes.appeareance.editor` | string | no |  |
| `attributes.appeareance.parameters` | object | no |  |
| `attributes.appearance.editor` | string | no |  |
| `attributes.appearance.fieldExtension` | string | no |  |
| `attributes.appearance.parameters` | object | no |  |
| `attributes.appearance.addons[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `PUT /fields/:fieldId` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-field.md) for the provider-specific parameters and requirements.

