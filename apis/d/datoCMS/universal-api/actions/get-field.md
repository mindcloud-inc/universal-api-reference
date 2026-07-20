# DatoCMS: Get Field



```
GET https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-field?connectionId=$CONNECTION_ID&fieldId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fieldId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/get-field?${params}`, {
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
| `fieldId` | string | yes | Field ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "apiKey": "string",
        "appearance": {
          "editor": "string",
          "parameters": {
            "toolbar": [
              "string"
            ]
          }
        },
        "deepFilteringEnabled": true,
        "defaultValue": "string",
        "fieldType": "string",
        "hint": "string",
        "label": "string",
        "localized": true,
        "position": 1
      },
      "id": "string",
      "relationships": {
        "fieldset": {
          "data": "string"
        },
        "itemType": {
          "data": {
            "id": "string",
            "type": "string"
          }
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.apiKey` | string |  |
| `attributes.appearance.editor` | string |  |
| `attributes.appearance.parameters.toolbar` | array<string> |  |
| `attributes.deepFilteringEnabled` | boolean |  |
| `attributes.defaultValue` | string |  |
| `attributes.fieldType` | string |  |
| `attributes.hint` | string |  |
| `attributes.label` | string |  |
| `attributes.localized` | boolean |  |
| `attributes.position` | number |  |
| `id` | string |  |
| `relationships.fieldset.data` | string |  |
| `relationships.itemType.data.id` | string |  |
| `relationships.itemType.data.type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `GET /fields/:fieldId` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-field.md) for the provider-specific parameters and requirements.

