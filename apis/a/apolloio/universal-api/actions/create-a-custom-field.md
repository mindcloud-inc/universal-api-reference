# Apollo: Create a Custom Field

Creates a new custom field in Apollo.

```
POST https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/create-a-custom-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apollo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/create-a-custom-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apolloio/latest/actions/create-a-custom-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `label` | string | no | Name of the custom field you want to create. Example: `Test Name` |
| `modality` | string | no | The modality of the custom field you want to create. Example: `contact` |
| `type` | string | no | What kind of custom field you want to create. Example: `textarea` |
| `meta` | object | no |  |
| `meta.maxLength` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field": {
        "category": "string",
        "contentCenterType": {},
        "context": [
          "string"
        ],
        "createdAt": "2026-05-07T12:00:00.000Z",
        "description": {},
        "editable": true,
        "example": {},
        "fieldName": "Ava Chen",
        "group": {},
        "iconClass": {},
        "id": "string",
        "isLocal": true,
        "label": "string",
        "meta": {
          "computedType": "string",
          "pushOnly": true,
          "visibilityStatus": "string"
        },
        "modality": "string",
        "parent": {},
        "projectWorkspaceId": {},
        "source": "string",
        "type": {}
      },
      "fieldGroups": [
        {
          "displayOrder": 1,
          "fieldIds": [
            "string"
          ],
          "id": "string",
          "modality": "string",
          "name": "Ava Chen",
          "teamId": "string",
          "type": "string"
        }
      ],
      "fields": [
        {
          "category": "string",
          "contentCenterType": {},
          "context": [
            "string"
          ],
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": {},
          "editable": true,
          "example": {},
          "fieldName": "Ava Chen",
          "group": {},
          "iconClass": {},
          "id": "string",
          "isLocal": true,
          "label": "string",
          "meta": {
            "computedType": "string",
            "pushOnly": true,
            "visibilityStatus": "string"
          },
          "modality": "string",
          "parent": {},
          "projectWorkspaceId": {},
          "source": "string",
          "type": {}
        }
      ],
      "typedCustomField": {
        "additionalMappedCrmField": {},
        "associatedModality": {},
        "contentCenterType": {},
        "dynamicFieldType": {},
        "id": "string",
        "isAiField": true,
        "isDynamicField": true,
        "isFormulaField": true,
        "isLocal": true,
        "isReadonly": {},
        "isReadonlyMappedCrmField": {},
        "jsonSchema": {},
        "mappedCrmField": {},
        "mirrored": true,
        "modality": "string",
        "name": "Ava Chen",
        "parentId": {},
        "picklistOptionsLastSyncedAt": {},
        "picklistValueSetId": {},
        "projectWorkspaceId": {},
        "systemName": {},
        "textFieldMaxLength": {},
        "type": {}
      },
      "typedCustomFields": [
        {
          "additionalMappedCrmField": {},
          "associatedModality": {},
          "contentCenterType": {},
          "dynamicFieldType": {},
          "id": "string",
          "isAiField": true,
          "isDynamicField": true,
          "isFormulaField": true,
          "isLocal": true,
          "isReadonly": {},
          "isReadonlyMappedCrmField": {},
          "jsonSchema": {},
          "mappedCrmField": {},
          "mirrored": true,
          "modality": "string",
          "name": "Ava Chen",
          "parentId": {},
          "picklistOptionsLastSyncedAt": {},
          "picklistValueSetId": {},
          "projectWorkspaceId": {},
          "systemName": {},
          "textFieldMaxLength": {},
          "type": {}
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field.category` | string |  |
| `field.contentCenterType` | object |  |
| `field.context[]` | string |  |
| `field.createdAt` | date |  |
| `field.description` | object |  |
| `field.editable` | boolean |  |
| `field.example` | object |  |
| `field.fieldName` | string |  |
| `field.group` | object |  |
| `field.iconClass` | object |  |
| `field.id` | string |  |
| `field.isLocal` | boolean |  |
| `field.label` | string |  |
| `field.meta.computedType` | string |  |
| `field.meta.pushOnly` | boolean |  |
| `field.meta.visibilityStatus` | string |  |
| `field.modality` | string |  |
| `field.parent` | object |  |
| `field.projectWorkspaceId` | object |  |
| `field.source` | string |  |
| `field.type` | object |  |
| `fieldGroups[].displayOrder` | number |  |
| `fieldGroups[].fieldIds[]` | string |  |
| `fieldGroups[].id` | string |  |
| `fieldGroups[].modality` | string |  |
| `fieldGroups[].name` | string |  |
| `fieldGroups[].teamId` | string |  |
| `fieldGroups[].type` | string |  |
| `fields[].category` | string |  |
| `fields[].contentCenterType` | object |  |
| `fields[].context[]` | string |  |
| `fields[].createdAt` | date |  |
| `fields[].description` | object |  |
| `fields[].editable` | boolean |  |
| `fields[].example` | object |  |
| `fields[].fieldName` | string |  |
| `fields[].group` | object |  |
| `fields[].iconClass` | object |  |
| `fields[].id` | string |  |
| `fields[].isLocal` | boolean |  |
| `fields[].label` | string |  |
| `fields[].meta.computedType` | string |  |
| `fields[].meta.pushOnly` | boolean |  |
| `fields[].meta.visibilityStatus` | string |  |
| `fields[].modality` | string |  |
| `fields[].parent` | object |  |
| `fields[].projectWorkspaceId` | object |  |
| `fields[].source` | string |  |
| `fields[].type` | object |  |
| `typedCustomField.additionalMappedCrmField` | object |  |
| `typedCustomField.associatedModality` | object |  |
| `typedCustomField.contentCenterType` | object |  |
| `typedCustomField.dynamicFieldType` | object |  |
| `typedCustomField.id` | string |  |
| `typedCustomField.isAiField` | boolean |  |
| `typedCustomField.isDynamicField` | boolean |  |
| `typedCustomField.isFormulaField` | boolean |  |
| `typedCustomField.isLocal` | boolean |  |
| `typedCustomField.isReadonly` | object |  |
| `typedCustomField.isReadonlyMappedCrmField` | object |  |
| `typedCustomField.jsonSchema` | object |  |
| `typedCustomField.mappedCrmField` | object |  |
| `typedCustomField.mirrored` | boolean |  |
| `typedCustomField.modality` | string |  |
| `typedCustomField.name` | string |  |
| `typedCustomField.parentId` | object |  |
| `typedCustomField.picklistOptionsLastSyncedAt` | object |  |
| `typedCustomField.picklistValueSetId` | object |  |
| `typedCustomField.projectWorkspaceId` | object |  |
| `typedCustomField.systemName` | object |  |
| `typedCustomField.textFieldMaxLength` | object |  |
| `typedCustomField.type` | object |  |
| `typedCustomFields[].additionalMappedCrmField` | object |  |
| `typedCustomFields[].associatedModality` | object |  |
| `typedCustomFields[].contentCenterType` | object |  |
| `typedCustomFields[].dynamicFieldType` | object |  |
| `typedCustomFields[].id` | string |  |
| `typedCustomFields[].isAiField` | boolean |  |
| `typedCustomFields[].isDynamicField` | boolean |  |
| `typedCustomFields[].isFormulaField` | boolean |  |
| `typedCustomFields[].isLocal` | boolean |  |
| `typedCustomFields[].isReadonly` | object |  |
| `typedCustomFields[].isReadonlyMappedCrmField` | object |  |
| `typedCustomFields[].jsonSchema` | object |  |
| `typedCustomFields[].mappedCrmField` | object |  |
| `typedCustomFields[].mirrored` | boolean |  |
| `typedCustomFields[].modality` | string |  |
| `typedCustomFields[].name` | string |  |
| `typedCustomFields[].parentId` | object |  |
| `typedCustomFields[].picklistOptionsLastSyncedAt` | object |  |
| `typedCustomFields[].picklistValueSetId` | object |  |
| `typedCustomFields[].projectWorkspaceId` | object |  |
| `typedCustomFields[].systemName` | object |  |
| `typedCustomFields[].textFieldMaxLength` | object |  |
| `typedCustomFields[].type` | object |  |

## Native endpoint

Through the native Apollo API, this operation is `POST v1/fields` (base URL `https://app.apollo.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-custom-field.md) for the provider-specific parameters and requirements.

