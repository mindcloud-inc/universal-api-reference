# DotCMS: List Content Types

Retrieves content type records from DotCMS.

```
GET https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-content-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DotCMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-content-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dotCMS/latest/actions/list-content-types?${params}`, {
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
      "entity": [
        {
          "baseType": "string",
          "clazz": "string",
          "defaultType": true,
          "description": "string",
          "detailPage": "string",
          "fixed": true,
          "folder": "string",
          "folderPath": "string",
          "host": "string",
          "icon": "string",
          "id": "string",
          "iDate": "2026-05-07T12:00:00.000Z",
          "layout": [
            {
              "columns": [
                {
                  "columnDivider": {
                    "clazz": "string",
                    "contentTypeId": "string",
                    "dataType": "string",
                    "fieldType": "string",
                    "fieldTypeLabel": "string",
                    "fixed": true,
                    "forceIncludeInApi": true,
                    "id": "string",
                    "iDate": "2026-05-07T12:00:00.000Z",
                    "indexed": true,
                    "listed": true,
                    "modDate": "2026-05-07T12:00:00.000Z",
                    "name": "Ava Chen",
                    "readOnly": true,
                    "required": true,
                    "searchable": true,
                    "sortOrder": 1,
                    "unique": true,
                    "variable": "string"
                  },
                  "fields": [
                    {
                      "clazz": "string",
                      "contentTypeId": "string",
                      "dataType": "string",
                      "fieldType": "string",
                      "fieldTypeLabel": "string",
                      "fixed": true,
                      "forceIncludeInApi": true,
                      "id": "string",
                      "iDate": "2026-05-07T12:00:00.000Z",
                      "indexed": true,
                      "listed": true,
                      "modDate": "2026-05-07T12:00:00.000Z",
                      "name": "Ava Chen",
                      "readOnly": true,
                      "required": true,
                      "searchable": true,
                      "sortOrder": 1,
                      "unique": true,
                      "variable": "string"
                    }
                  ]
                }
              ],
              "divider": {
                "clazz": "string",
                "contentTypeId": "string",
                "dataType": "string",
                "fieldType": "string",
                "fieldTypeLabel": "string",
                "fixed": true,
                "forceIncludeInApi": true,
                "id": "string",
                "iDate": "2026-05-07T12:00:00.000Z",
                "indexed": true,
                "listed": true,
                "modDate": "2026-05-07T12:00:00.000Z",
                "name": "Ava Chen",
                "readOnly": true,
                "required": true,
                "searchable": true,
                "sortOrder": 1,
                "unique": true,
                "variable": "string"
              }
            }
          ],
          "modDate": "2026-05-07T12:00:00.000Z",
          "multilingualable": true,
          "name": "Ava Chen",
          "nEntries": 1,
          "siteName": "Ava Chen",
          "sortOrder": 1,
          "system": true,
          "systemActionMappings": [
            {
              "identifier": "string",
              "owner": {
                "defaultType": true,
                "description": "string",
                "detailPage": "string",
                "expireDateVar": {},
                "fixed": true,
                "folder": "string",
                "folderPath": "string",
                "host": "string",
                "icon": "string",
                "id": "string",
                "iDate": "2026-05-07T12:00:00.000Z",
                "modDate": "2026-05-07T12:00:00.000Z",
                "multilingualable": true,
                "name": "Ava Chen",
                "owner": {},
                "publishDateVar": {},
                "siteName": "Ava Chen",
                "sortOrder": 1,
                "system": true,
                "urlMapPattern": "https://example.com",
                "variable": "string",
                "versionable": true
              },
              "ownerContentType": true,
              "ownerScheme": true,
              "systemAction": "string",
              "workflowAction": {
                "assignable": true,
                "commentable": true,
                "condition": "string",
                "hasArchiveActionlet": true,
                "hasCommentActionlet": true,
                "hasDeleteActionlet": true,
                "hasDestroyActionlet": true,
                "hasMoveActionletActionlet": true,
                "hasMoveActionletHasPathActionlet": true,
                "hasOnlyBatchActionlet": true,
                "hasPublishActionlet": true,
                "hasPushPublishActionlet": true,
                "hasResetActionlet": true,
                "hasSaveActionlet": true,
                "hasUnarchiveActionlet": true,
                "hasUnpublishActionlet": true,
                "icon": "string",
                "id": "string",
                "metadata": {},
                "name": "Ava Chen",
                "nextAssign": "string",
                "nextStep": "string",
                "nextStepCurrentStep": true,
                "order": 1,
                "owner": {},
                "roleHierarchyForAssign": true,
                "schemeId": "string",
                "showOn": [
                  "string"
                ]
              }
            }
          ],
          "urlMapPattern": "https://example.com",
          "variable": "string",
          "versionable": true,
          "workflows": [
            {
              "archived": true,
              "creationDate": 1,
              "defaultScheme": true,
              "description": "string",
              "entryActionId": {},
              "id": "string",
              "mandatory": true,
              "modDate": "2026-05-07T12:00:00.000Z",
              "name": "Ava Chen",
              "system": true,
              "variableName": "Ava Chen"
            }
          ]
        }
      ],
      "pagination": {
        "currentPage": 1,
        "perPage": 1,
        "totalEntries": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `entity[].baseType` | string |  |
| `entity[].clazz` | string |  |
| `entity[].defaultType` | boolean |  |
| `entity[].description` | string |  |
| `entity[].detailPage` | string |  |
| `entity[].fixed` | boolean |  |
| `entity[].folder` | string |  |
| `entity[].folderPath` | string |  |
| `entity[].host` | string |  |
| `entity[].icon` | string |  |
| `entity[].id` | string |  |
| `entity[].iDate` | date |  |
| `entity[].layout[].columns[].columnDivider.clazz` | string |  |
| `entity[].layout[].columns[].columnDivider.contentTypeId` | string |  |
| `entity[].layout[].columns[].columnDivider.dataType` | string |  |
| `entity[].layout[].columns[].columnDivider.fieldType` | string |  |
| `entity[].layout[].columns[].columnDivider.fieldTypeLabel` | string |  |
| `entity[].layout[].columns[].columnDivider.fixed` | boolean |  |
| `entity[].layout[].columns[].columnDivider.forceIncludeInApi` | boolean |  |
| `entity[].layout[].columns[].columnDivider.id` | string |  |
| `entity[].layout[].columns[].columnDivider.iDate` | date |  |
| `entity[].layout[].columns[].columnDivider.indexed` | boolean |  |
| `entity[].layout[].columns[].columnDivider.listed` | boolean |  |
| `entity[].layout[].columns[].columnDivider.modDate` | date |  |
| `entity[].layout[].columns[].columnDivider.name` | string |  |
| `entity[].layout[].columns[].columnDivider.readOnly` | boolean |  |
| `entity[].layout[].columns[].columnDivider.required` | boolean |  |
| `entity[].layout[].columns[].columnDivider.searchable` | boolean |  |
| `entity[].layout[].columns[].columnDivider.sortOrder` | number |  |
| `entity[].layout[].columns[].columnDivider.unique` | boolean |  |
| `entity[].layout[].columns[].columnDivider.variable` | string |  |
| `entity[].layout[].columns[].fields[].clazz` | string |  |
| `entity[].layout[].columns[].fields[].contentTypeId` | string |  |
| `entity[].layout[].columns[].fields[].dataType` | string |  |
| `entity[].layout[].columns[].fields[].fieldType` | string |  |
| `entity[].layout[].columns[].fields[].fieldTypeLabel` | string |  |
| `entity[].layout[].columns[].fields[].fixed` | boolean |  |
| `entity[].layout[].columns[].fields[].forceIncludeInApi` | boolean |  |
| `entity[].layout[].columns[].fields[].id` | string |  |
| `entity[].layout[].columns[].fields[].iDate` | date |  |
| `entity[].layout[].columns[].fields[].indexed` | boolean |  |
| `entity[].layout[].columns[].fields[].listed` | boolean |  |
| `entity[].layout[].columns[].fields[].modDate` | date |  |
| `entity[].layout[].columns[].fields[].name` | string |  |
| `entity[].layout[].columns[].fields[].readOnly` | boolean |  |
| `entity[].layout[].columns[].fields[].required` | boolean |  |
| `entity[].layout[].columns[].fields[].searchable` | boolean |  |
| `entity[].layout[].columns[].fields[].sortOrder` | number |  |
| `entity[].layout[].columns[].fields[].unique` | boolean |  |
| `entity[].layout[].columns[].fields[].variable` | string |  |
| `entity[].layout[].divider.clazz` | string |  |
| `entity[].layout[].divider.contentTypeId` | string |  |
| `entity[].layout[].divider.dataType` | string |  |
| `entity[].layout[].divider.fieldType` | string |  |
| `entity[].layout[].divider.fieldTypeLabel` | string |  |
| `entity[].layout[].divider.fixed` | boolean |  |
| `entity[].layout[].divider.forceIncludeInApi` | boolean |  |
| `entity[].layout[].divider.id` | string |  |
| `entity[].layout[].divider.iDate` | date |  |
| `entity[].layout[].divider.indexed` | boolean |  |
| `entity[].layout[].divider.listed` | boolean |  |
| `entity[].layout[].divider.modDate` | date |  |
| `entity[].layout[].divider.name` | string |  |
| `entity[].layout[].divider.readOnly` | boolean |  |
| `entity[].layout[].divider.required` | boolean |  |
| `entity[].layout[].divider.searchable` | boolean |  |
| `entity[].layout[].divider.sortOrder` | number |  |
| `entity[].layout[].divider.unique` | boolean |  |
| `entity[].layout[].divider.variable` | string |  |
| `entity[].modDate` | date |  |
| `entity[].multilingualable` | boolean |  |
| `entity[].name` | string |  |
| `entity[].nEntries` | number |  |
| `entity[].siteName` | string |  |
| `entity[].sortOrder` | number |  |
| `entity[].system` | boolean |  |
| `entity[].systemActionMappings[].identifier` | string |  |
| `entity[].systemActionMappings[].owner.defaultType` | boolean |  |
| `entity[].systemActionMappings[].owner.description` | string |  |
| `entity[].systemActionMappings[].owner.detailPage` | string |  |
| `entity[].systemActionMappings[].owner.expireDateVar` | object |  |
| `entity[].systemActionMappings[].owner.fixed` | boolean |  |
| `entity[].systemActionMappings[].owner.folder` | string |  |
| `entity[].systemActionMappings[].owner.folderPath` | string |  |
| `entity[].systemActionMappings[].owner.host` | string |  |
| `entity[].systemActionMappings[].owner.icon` | string |  |
| `entity[].systemActionMappings[].owner.id` | string |  |
| `entity[].systemActionMappings[].owner.iDate` | date |  |
| `entity[].systemActionMappings[].owner.modDate` | date |  |
| `entity[].systemActionMappings[].owner.multilingualable` | boolean |  |
| `entity[].systemActionMappings[].owner.name` | string |  |
| `entity[].systemActionMappings[].owner.owner` | object |  |
| `entity[].systemActionMappings[].owner.publishDateVar` | object |  |
| `entity[].systemActionMappings[].owner.siteName` | string |  |
| `entity[].systemActionMappings[].owner.sortOrder` | number |  |
| `entity[].systemActionMappings[].owner.system` | boolean |  |
| `entity[].systemActionMappings[].owner.urlMapPattern` | string |  |
| `entity[].systemActionMappings[].owner.variable` | string |  |
| `entity[].systemActionMappings[].owner.versionable` | boolean |  |
| `entity[].systemActionMappings[].ownerContentType` | boolean |  |
| `entity[].systemActionMappings[].ownerScheme` | boolean |  |
| `entity[].systemActionMappings[].systemAction` | string |  |
| `entity[].systemActionMappings[].workflowAction.assignable` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.commentable` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.condition` | string |  |
| `entity[].systemActionMappings[].workflowAction.hasArchiveActionlet` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.hasCommentActionlet` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.hasDeleteActionlet` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.hasDestroyActionlet` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.hasMoveActionletActionlet` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.hasMoveActionletHasPathActionlet` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.hasOnlyBatchActionlet` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.hasPublishActionlet` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.hasPushPublishActionlet` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.hasResetActionlet` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.hasSaveActionlet` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.hasUnarchiveActionlet` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.hasUnpublishActionlet` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.icon` | string |  |
| `entity[].systemActionMappings[].workflowAction.id` | string |  |
| `entity[].systemActionMappings[].workflowAction.metadata` | object |  |
| `entity[].systemActionMappings[].workflowAction.name` | string |  |
| `entity[].systemActionMappings[].workflowAction.nextAssign` | string |  |
| `entity[].systemActionMappings[].workflowAction.nextStep` | string |  |
| `entity[].systemActionMappings[].workflowAction.nextStepCurrentStep` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.order` | number |  |
| `entity[].systemActionMappings[].workflowAction.owner` | object |  |
| `entity[].systemActionMappings[].workflowAction.roleHierarchyForAssign` | boolean |  |
| `entity[].systemActionMappings[].workflowAction.schemeId` | string |  |
| `entity[].systemActionMappings[].workflowAction.showOn[]` | string |  |
| `entity[].urlMapPattern` | string |  |
| `entity[].variable` | string |  |
| `entity[].versionable` | boolean |  |
| `entity[].workflows[].archived` | boolean |  |
| `entity[].workflows[].creationDate` | number |  |
| `entity[].workflows[].defaultScheme` | boolean |  |
| `entity[].workflows[].description` | string |  |
| `entity[].workflows[].entryActionId` | object |  |
| `entity[].workflows[].id` | string |  |
| `entity[].workflows[].mandatory` | boolean |  |
| `entity[].workflows[].modDate` | date |  |
| `entity[].workflows[].name` | string |  |
| `entity[].workflows[].system` | boolean |  |
| `entity[].workflows[].variableName` | string |  |
| `pagination.currentPage` | number |  |
| `pagination.perPage` | number |  |
| `pagination.totalEntries` | number |  |

## Native endpoint

Through the native DotCMS API, this operation is `GET /api/v1/contenttype` (base URL `https://demo.dotcms.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-content-types.md) for the provider-specific parameters and requirements.

