# DatoCMS: Duplicate Model



```
POST https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/duplicate-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/duplicate-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemTypeId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/duplicate-model', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemTypeId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemTypeId` | string | yes | Model ID or API key. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "allLocalesRequired": true,
        "apiKey": "string",
        "collectionAppearance": "string",
        "draftModeActive": true,
        "draftSavingActive": true,
        "hasSingletonItem": true,
        "hint": "string",
        "inverseRelationshipsEnabled": true,
        "modularBlock": true,
        "name": "Ava Chen",
        "orderingDirection": "string",
        "orderingMeta": "string",
        "singleton": true,
        "sortable": true,
        "tree": true
      },
      "id": "string",
      "meta": {
        "hasSingletonItem": true
      },
      "relationships": {
        "excerptField": {
          "data": "string"
        },
        "fields": {
          "data": [
            {
              "id": "string",
              "type": "string"
            }
          ]
        },
        "imagePreviewField": {
          "data": "string"
        },
        "orderingField": {
          "data": "string"
        },
        "presentationImageField": {
          "data": "string"
        },
        "presentationTitleField": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "singletonItem": {
          "data": "string"
        },
        "titleField": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "workflow": {
          "data": "string"
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
| `attributes.allLocalesRequired` | boolean |  |
| `attributes.apiKey` | string |  |
| `attributes.collectionAppearance` | string |  |
| `attributes.draftModeActive` | boolean |  |
| `attributes.draftSavingActive` | boolean |  |
| `attributes.hasSingletonItem` | boolean |  |
| `attributes.hint` | string |  |
| `attributes.inverseRelationshipsEnabled` | boolean |  |
| `attributes.modularBlock` | boolean |  |
| `attributes.name` | string |  |
| `attributes.orderingDirection` | string |  |
| `attributes.orderingMeta` | string |  |
| `attributes.singleton` | boolean |  |
| `attributes.sortable` | boolean |  |
| `attributes.tree` | boolean |  |
| `id` | string |  |
| `meta.hasSingletonItem` | boolean |  |
| `relationships.excerptField.data` | string |  |
| `relationships.fields.data[].id` | string |  |
| `relationships.fields.data[].type` | string |  |
| `relationships.imagePreviewField.data` | string |  |
| `relationships.orderingField.data` | string |  |
| `relationships.presentationImageField.data` | string |  |
| `relationships.presentationTitleField.data.id` | string |  |
| `relationships.presentationTitleField.data.type` | string |  |
| `relationships.singletonItem.data` | string |  |
| `relationships.titleField.data.id` | string |  |
| `relationships.titleField.data.type` | string |  |
| `relationships.workflow.data` | string |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `POST /item-types/:itemTypeId/duplicate` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-model.md) for the provider-specific parameters and requirements.

