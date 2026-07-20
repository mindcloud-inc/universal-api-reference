# DatoCMS: Update Model



```
PUT https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemTypeId": "string",
  "attributes": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/update-model', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemTypeId": "string",
    "attributes": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemTypeId` | string | yes | Model ID or API key. |
| `attributes` | object | yes | Model attributes payload. Example: `[object Object]`. |
| `attributes.name` | string | no |  |
| `attributes.apiKey` | string | no |  |
| `attributes.collectionAppeareance` | string | no |  |
| `attributes.collectionAppearance` | string | no |  |
| `attributes.singleton` | boolean | no |  |
| `attributes.allLocalesRequired` | boolean | no |  |
| `attributes.sortable` | boolean | no |  |
| `attributes.modularBlock` | boolean | no |  |
| `attributes.draftModeActive` | boolean | no |  |
| `attributes.draftSavingActive` | boolean | no |  |
| `attributes.tree` | boolean | no |  |
| `attributes.orderingDirection` | string | no |  |
| `attributes.orderingMeta` | string | no |  |
| `attributes.hasSingletonItem` | boolean | no |  |
| `attributes.hint` | string | no |  |
| `attributes.inverseRelationshipsEnabled` | boolean | no |  |

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

Through the native DatoCMS API, this operation is `PUT /item-types/:itemTypeId` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-model.md) for the provider-specific parameters and requirements.

