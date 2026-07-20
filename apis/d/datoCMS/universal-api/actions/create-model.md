# DatoCMS: Create Model



```
POST https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-model
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DatoCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-model" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "modelName": "MindCloud Articles",
  "modelApiKey": "mindcloud_articles"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/datoCMS/latest/actions/create-model', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "modelName": "MindCloud Articles",
    "modelApiKey": "mindcloud_articles"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `modelName` | string | yes | Example: `MindCloud Articles`. |
| `modelApiKey` | string | yes | Example: `mindcloud_articles`. |
| `singleton` | boolean | no | Set true when the model should allow only one record. Example: `false`. |
| `allLocalesRequired` | boolean | no | Require all locales for localized fields. Example: `false`. |
| `sortable` | boolean | no | Allow manual sorting of records. Example: `false`. |
| `modularBlock` | boolean | no | Create the model as a modular block model. Example: `false`. |
| `draftModeActive` | boolean | no | Enable draft mode for records in this model. Example: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bodyId` | string | no | Optional custom ID for the new model. Example: `model_custom_id`. |
| `inverseRelationshipsEnabled` | boolean | no | Enable inverse relationships on this model. Example: `false`. |
| `draftSavingActive` | boolean | no | Enable partial draft-saving behavior. Example: `false`. |
| `tree` | boolean | no | Enable tree/hierarchical records for this model. Example: `false`. |
| `collectionAppearance` | string | no | Collection appearance mode for the model. Example: `compact`. |
| `orderingDirection` | string | no | Default ordering direction for sorted collections. Example: `_created_at_DESC`. |
| `orderingMeta` | string | no | Ordering metadata configuration object. Example: `[object Object]`. |
| `hint` | string | no | Optional hint shown to editors for this model. Example: `Editorial model hint`. |
| `orderingFieldId` | string | no | Field ID used for default ordering. Example: `field_123`. |
| `presentationTitleFieldId` | string | no | Field ID used as presentation title. Example: `field_123`. |
| `presentationImageFieldId` | string | no | Field ID used as presentation image. Example: `field_123`. |
| `titleFieldId` | string | no | Field ID used as model title field. Example: `field_123`. |
| `imagePreviewFieldId` | string | no | Field ID used as image preview field. Example: `field_123`. |
| `excerptFieldId` | string | no | Field ID used as excerpt field. Example: `field_123`. |
| `workflowId` | string | no | Workflow ID associated with this model. Example: `workflow_123`. |
| `skipMenuItemCreation` | boolean | no | Create the model without creating a menu item. Example: `false`. |
| `menuItemId` | string | no | Attach this model to an existing menu item. Example: `12345`. |
| `schemaMenuItemId` | string | no | Set the menu item under which this schema is created. Example: `67890`. |
| `orderingMeta.field` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "meta": {},
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
| `attributes` | object | Model attributes |
| `id` | string | Model ID |
| `meta` | object | Metadata |
| `relationships` | object | Related resources |
| `type` | string | Resource type |

## Native endpoint

Through the native DatoCMS API, this operation is `POST /item-types` (base URL `https://site-api.datocms.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-model.md) for the provider-specific parameters and requirements.

