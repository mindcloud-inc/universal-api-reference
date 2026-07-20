# DatoCMS: Create Field



```
POST https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemTypeId": "drhAV2GeQC6f8ScV_Tq5Pw",
  "fieldLabel": "Title",
  "fieldApiKey": "title",
  "fieldType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemTypeId": "drhAV2GeQC6f8ScV_Tq5Pw",
    "fieldLabel": "Title",
    "fieldApiKey": "title",
    "fieldType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemTypeId` | string | yes | Example: `drhAV2GeQC6f8ScV_Tq5Pw`. |
| `fieldLabel` | string | yes | Example: `Title`. |
| `fieldApiKey` | string | yes | Example: `title`. |
| `fieldType` | string | yes | Default: `string`. Example: `string`. |
| `localized` | boolean | no | Set true if this field should be localized. Example: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bodyId` | string | no | Optional custom ID for the new field. Example: `field_custom_id`. |
| `position` | number | no | Position index in the field ordering for the model. Example: `1`. |
| `hint` | string | no | Optional editor hint for this field. Example: `Shown in the editor UI`. |
| `validators` | object | no | Field validator configuration object. Example: `[object Object]`. |
| `appearance` | object | no | Editor appearance configuration object. Example: `[object Object]`. |
| `defaultValue` | object | no | Default value object for the field. Example: `[object Object]`. |
| `deepFilteringEnabled` | boolean | no | Enable deep filtering support for this field. Example: `false`. |
| `fieldsetId` | string | no | Existing fieldset ID to attach this field to. Example: `fieldset_123`. |
| `forceNewFieldset` | boolean | no | Create a new fieldset instead of reusing an existing one. Example: `false`. |
| `appearance.parameters.heading` | boolean | no |  |
| `appearance.addons[]` | array<object> | no |  |
| `appearance.addons[].id` | string | no |  |
| `appearance.addons[].fieldExtension` | string | no |  |
| `appearance.addons[].parameters` | object | no |  |
| `appearance.editor` | string | no |  |
| `appearance.fieldExtension` | string | no |  |
| `appearance.parameters` | object | no |  |
| `validators.required` | object | no |  |
| `defaultValue.en` | string | no |  |
| `defaultValue.it` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Field attributes |
| `id` | string | Field ID |
| `relationships` | object | Related resources |
| `type` | string | Resource type |

## Native endpoint

Through the native DatoCMS API, this operation is `POST /item-types/:itemTypeId/fields` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-field.md) for the provider-specific parameters and requirements.

