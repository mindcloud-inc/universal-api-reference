# Ortto: Modify Custom Activity Definition



```
PUT https://connect.mindcloud.co/v1/universal/ortto/latest/actions/modify-custom-activity-definition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ortto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/modify-custom-activity-definition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityFieldId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ortto/latest/actions/modify-custom-activity-definition', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityFieldId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activityFieldId` | string | yes | Custom activity field ID to modify. |
| `name` | string | no | Updated custom activity definition name. |
| `state` | string | no | Activity state such as live. |
| `iconId` | string | no | Ortto icon ID shown for the activity. |
| `trackConversionValue` | boolean | no | Whether the activity tracks conversion value. |
| `touch` | boolean | no | Whether the activity updates first seen and last seen. |
| `filterable` | boolean | no | Whether the activity can be used in filters and reports. |
| `visibleInFeeds` | boolean | no | Whether the activity is shown in feeds. |
| `displayStyle` | object | no | Display style object with type and optional title or attribute references. |
| `attributes[]` | array<object> | no | Array of custom activity attribute definitions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customActivity": {
        "activityFieldId": "string",
        "attributes": [
          {
            "displayType": "string",
            "fieldId": "string",
            "liquidName": "Ava Chen",
            "name": "Ava Chen"
          }
        ],
        "createdAt": "string",
        "createdBy": "string",
        "displayMode": {
          "type": "string"
        },
        "editedAt": "string",
        "filterable": true,
        "iconId": "string",
        "name": "Ava Chen",
        "state": "string",
        "touch": true,
        "trackConversionValue": true,
        "visibleInFeeds": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customActivity.activityFieldId` | string |  |
| `customActivity.attributes[].displayType` | string |  |
| `customActivity.attributes[].fieldId` | string |  |
| `customActivity.attributes[].liquidName` | string |  |
| `customActivity.attributes[].name` | string |  |
| `customActivity.createdAt` | string |  |
| `customActivity.createdBy` | string |  |
| `customActivity.displayMode.type` | string |  |
| `customActivity.editedAt` | string |  |
| `customActivity.filterable` | boolean |  |
| `customActivity.iconId` | string |  |
| `customActivity.name` | string |  |
| `customActivity.state` | string |  |
| `customActivity.touch` | boolean |  |
| `customActivity.trackConversionValue` | boolean |  |
| `customActivity.visibleInFeeds` | boolean |  |

## Native endpoint

Through the native Ortto API, this operation is `PUT /definitions/activity/modify` (base URL `{{credentials.apiBaseUrl}}/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/modify-custom-activity-definition.md) for the provider-specific parameters and requirements.

