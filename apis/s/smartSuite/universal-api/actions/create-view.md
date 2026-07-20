# SmartSuite: Create View

Creates a new view in SmartSuite.

```
POST https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/create-view
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartSuite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/create-view" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tableId": "69b45da87cb40fc74dbb4b84",
  "solutionId": "69b45da87cb40fc74dbb4b83",
  "label": "MC Test View",
  "viewMode": "grid",
  "state": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/create-view', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tableId": "69b45da87cb40fc74dbb4b84",
    "solutionId": "69b45da87cb40fc74dbb4b83",
    "label": "MC Test View",
    "viewMode": "grid",
    "state": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tableId` | string | yes | The SmartSuite table ID the view belongs to. Example: `69b45da87cb40fc74dbb4b84`. |
| `solutionId` | string | yes | The SmartSuite solution ID containing the table. Example: `69b45da87cb40fc74dbb4b83`. |
| `label` | string | yes | The label shown for the new SmartSuite view. Example: `MC Test View`. |
| `viewMode` | string | yes | The SmartSuite view mode, such as grid. Example: `grid`. |
| `state` | object | yes | The SmartSuite view state object, including visible fields and filter settings. Example: `[object Object]`. |
| `description` | string | no | Optional description for the view. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `order` | number | no | Optional ordering value for the view. Example: `99`. |
| `autosave` | boolean | no | Whether the SmartSuite view autosaves changes. Default: `false`. |
| `isDirty` | boolean | no | Internal SmartSuite dirty-state flag for the view. Default: `false`. |
| `isLocked` | boolean | no | Whether the SmartSuite view is locked. Default: `false`. |
| `isPasswordProtected` | boolean | no | Whether the SmartSuite view is password protected. Default: `false`. |
| `isPrivate` | boolean | no | Whether the SmartSuite view is private. Default: `false`. |
| `mapState` | object | no | Map configuration state for map views. Default: `{}`. Example: `[object Object]`. |
| `sharingAllowAllFields` | boolean | no | Whether shared views expose all fields. Default: `false`. |
| `sharingAllowCopy` | boolean | no | Whether shared views allow copying. Default: `false`. |
| `sharingAllowExport` | boolean | no | Whether shared views allow export. Default: `false`. |
| `sharingAllowOpenRecords` | boolean | no | Whether shared views allow opening records. Default: `false`. |
| `sharingEnabled` | boolean | no | Whether sharing is enabled for the view. Default: `false`. |
| `sharingHash` | string | no | Optional SmartSuite sharing hash. |
| `sharingPassword` | string | no | Optional password for the shared view. |
| `sharingShowToolbar` | boolean | no | Whether shared views show the toolbar. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "application": "string",
      "autosave": true,
      "dashboard": {},
      "description": "string",
      "document": {},
      "formState": {},
      "id": "string",
      "isDescriptionEnabled": true,
      "isDescriptionInline": true,
      "isLocked": true,
      "isPasswordProtected": true,
      "isPrivate": true,
      "label": "string",
      "order": 1,
      "owner": "string",
      "parentFolder": {},
      "permissions": {},
      "privateMember": {},
      "sharingAllowAllFields": true,
      "sharingAllowCopy": true,
      "sharingAllowExport": true,
      "sharingAllowOpenRecord": true,
      "sharingEnabled": true,
      "sharingHash": "string",
      "sharingPassword": {},
      "sharingShowRecordsList": true,
      "sharingShowToolbar": true,
      "solution": "string",
      "state": {
        "fieldsWindow": {
          "fixedFieldsCount": 1,
          "visibleFields": [
            "string"
          ]
        },
        "filterWindow": {
          "filter": {
            "operator": "string"
          },
          "opened": true
        }
      },
      "viewMode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `application` | string |  |
| `autosave` | boolean |  |
| `dashboard` | object |  |
| `description` | string |  |
| `document` | object |  |
| `formState` | object |  |
| `id` | string |  |
| `isDescriptionEnabled` | boolean |  |
| `isDescriptionInline` | boolean |  |
| `isLocked` | boolean |  |
| `isPasswordProtected` | boolean |  |
| `isPrivate` | boolean |  |
| `label` | string |  |
| `order` | number |  |
| `owner` | string |  |
| `parentFolder` | object |  |
| `permissions` | object |  |
| `privateMember` | object |  |
| `sharingAllowAllFields` | boolean |  |
| `sharingAllowCopy` | boolean |  |
| `sharingAllowExport` | boolean |  |
| `sharingAllowOpenRecord` | boolean |  |
| `sharingEnabled` | boolean |  |
| `sharingHash` | string |  |
| `sharingPassword` | object |  |
| `sharingShowRecordsList` | boolean |  |
| `sharingShowToolbar` | boolean |  |
| `solution` | string |  |
| `state.fieldsWindow.fixedFieldsCount` | number |  |
| `state.fieldsWindow.visibleFields[]` | string |  |
| `state.filterWindow.filter.operator` | string |  |
| `state.filterWindow.opened` | boolean |  |
| `viewMode` | string |  |

## Native endpoint

Through the native SmartSuite API, this operation is `POST /reports/` (base URL `https://app.smartsuite.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-view.md) for the provider-specific parameters and requirements.

