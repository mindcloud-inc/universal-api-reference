# Swipe One: Create Event Definition



```
POST https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-event-definition
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swipe One `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-event-definition" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "name": "Ava Chen",
  "label": "string",
  "properties[]": [
    {}
  ],
  "recordSummary": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swipeOne/latest/actions/create-event-definition', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "name": "Ava Chen",
    "label": "string",
    "properties[]": [{}],
    "recordSummary": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes |  |
| `name` | string | yes |  |
| `label` | string | yes |  |
| `properties[]` | array<object> | yes |  |
| `recordSummary` | boolean | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "eventDefinition": {
          "createdAt": "string",
          "createdBy": {
            "id": "string",
            "name": "Ava Chen",
            "type": "string"
          },
          "Id": "string",
          "label": "string",
          "name": "Ava Chen",
          "properties": [
            {
              "dataType": "string",
              "fieldType": "string",
              "label": "string",
              "name": "Ava Chen"
            }
          ],
          "recordSummary": true,
          "updatedAt": "string",
          "V": 1,
          "workspaceId": "string"
        }
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.eventDefinition.createdAt` | string |  |
| `data.eventDefinition.createdBy.id` | string |  |
| `data.eventDefinition.createdBy.name` | string |  |
| `data.eventDefinition.createdBy.type` | string |  |
| `data.eventDefinition.Id` | string |  |
| `data.eventDefinition.label` | string |  |
| `data.eventDefinition.name` | string |  |
| `data.eventDefinition.properties[].dataType` | string |  |
| `data.eventDefinition.properties[].fieldType` | string |  |
| `data.eventDefinition.properties[].label` | string |  |
| `data.eventDefinition.properties[].name` | string |  |
| `data.eventDefinition.recordSummary` | boolean |  |
| `data.eventDefinition.updatedAt` | string |  |
| `data.eventDefinition.V` | number |  |
| `data.eventDefinition.workspaceId` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Swipe One API, this operation is `POST /workspaces/:workspaceId/event-definitions` (base URL `https://api.swipeone.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-event-definition.md) for the provider-specific parameters and requirements.

