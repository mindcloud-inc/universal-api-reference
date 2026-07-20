# SafetyCulture: Create Action

Creates a new action in SafetyCulture.

```
POST https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/create-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/create-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/create-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | no | The unique identifier of the action If not provided, UUID will be generated server side. |
| `title` | string | yes | Required. Title of the action Title is limited to only 255 characters max. |
| `description` | string | no | Description of the action (maximum 30000 characters). |
| `collaborators[]` | array<object> | no | The collaborators involved into this action. |
| `priorityId` | string | no | ID of the action's priority If not set, this action will be stored with the default priority(none). |
| `statusId` | string | no | ID of the action's status If not set, this action will be stored with the default status(to do). |
| `createdAt` | date | no | Date and time this action was created. |
| `dueAt` | date | no | Date/time this action is due |
| `inspectionId` | string | no | ID of the inspection the action belongs to If not set, this action is a standalone action and the inspection ID will be null. |
| `inspectionItemId` | string | no | ID of the item in the inspection associated with the action |
| `templateId` | string | no | If a template ID is provided then an inspection ID must be provided. If not set, this action is a standalone action and the template ID will be null. |
| `siteId` | string | no | ID of the Site associated with the action. |
| `references[]` | array<object> | no | Array of references attached to this action. |
| `assetId` | string | no | ID of the Asset associated with the action |
| `labelIds[]` | array<string> | no | IDs of the labels associated with the action. |
| `type` | object | no | The type to create an action in. |
| `fieldValues[]` | array<object> | no | Array of custom fields and their values to create with the action. |
| `templateIds[]` | array<string> | no | The list of templates to be linked to the action. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actionId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actionId` | string |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `POST /tasks/v1/actions` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-action.md) for the provider-specific parameters and requirements.

