# DatoCMS: List Models



```
GET https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-models
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-models?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/list-models?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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
        "hint": {},
        "inverseRelationshipsEnabled": true,
        "modularBlock": true,
        "name": "Ava Chen",
        "orderingDirection": {},
        "orderingMeta": {},
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
          "data": {}
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
          "data": {}
        },
        "orderingField": {
          "data": {}
        },
        "presentationImageField": {
          "data": {}
        },
        "presentationTitleField": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "singletonItem": {
          "data": {}
        },
        "titleField": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "workflow": {
          "data": {}
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
| `attributes.hint` | object |  |
| `attributes.inverseRelationshipsEnabled` | boolean |  |
| `attributes.modularBlock` | boolean |  |
| `attributes.name` | string |  |
| `attributes.orderingDirection` | object |  |
| `attributes.orderingMeta` | object |  |
| `attributes.singleton` | boolean |  |
| `attributes.sortable` | boolean |  |
| `attributes.tree` | boolean |  |
| `id` | string |  |
| `meta.hasSingletonItem` | boolean |  |
| `relationships.excerptField.data` | object |  |
| `relationships.fields.data[].id` | string |  |
| `relationships.fields.data[].type` | string |  |
| `relationships.imagePreviewField.data` | object |  |
| `relationships.orderingField.data` | object |  |
| `relationships.presentationImageField.data` | object |  |
| `relationships.presentationTitleField.data.id` | string |  |
| `relationships.presentationTitleField.data.type` | string |  |
| `relationships.singletonItem.data` | object |  |
| `relationships.titleField.data.id` | string |  |
| `relationships.titleField.data.type` | string |  |
| `relationships.workflow.data` | object |  |
| `type` | string |  |

## Native endpoint

Through the native DatoCMS API, this operation is `GET /item-types` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-models.md) for the provider-specific parameters and requirements.

