# Moderation API: Update An Action

Updates a moderation action in Moderation API.

```
PUT https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/update-an-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/update-an-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/update-an-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the action to update. |
| `key` | string | no | User defined key of the action. |
| `name` | string | no | The name of the action. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | The description of the action. |
| `type` | string | no | The type of the action. |
| `builtIn` | boolean | no | Whether the action is a built-in action or a custom one. |
| `queueBehaviour` | string | no | Whether the action resolves and removes the item, unresolves and re-add it to the queue, or does not change the resolve status. |
| `filterInQueueIds[]` | array<string> | no | The IDs of the queues the action is available in. |
| `position` | string | no | Show the action in all queues, selected queues or no queues (to use via API only). |
| `possibleValues[]` | array<object> | no | The possible values of the action. The user will be prompted to select one of these values when executing the action. |
| `valueRequired` | boolean | no | Whether the action requires a value to be executed. |
| `freeText` | boolean | no | Whether the action allows any text to be entered as a value or if it must be one of the possible values. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "builtIn": true,
      "createdAt": "string",
      "description": "string",
      "filterInQueueIds": [
        "string"
      ],
      "freeText": true,
      "id": "string",
      "key": "string",
      "name": "Ava Chen",
      "position": "string",
      "possibleValues": [
        {}
      ],
      "queueBehaviour": "string",
      "type": "string",
      "valueRequired": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `builtIn` | boolean |  |
| `createdAt` | string | The date the action was created. |
| `description` | string |  |
| `filterInQueueIds` | array<string> | The IDs of the queues the action is available in. |
| `freeText` | boolean | Whether the action allows any text to be entered as a value or if it must be one of the possible values. |
| `id` | string | The ID of the action. |
| `key` | string |  |
| `name` | string | The name of the action. |
| `position` | string | Show the action in all queues, selected queues or no queues (to use via API only). |
| `possibleValues` | array<object> | The possible values of the action. The user will be prompted to select one of these values when executing the action. |
| `queueBehaviour` | string | Whether the action resolves and removes the item, unresolves and re-add it to the queue, or does not change the resolve status. |
| `type` | string |  |
| `valueRequired` | boolean | Whether the action requires a value to be executed. |

## Native endpoint

Through the native Moderation API API, this operation is `PUT /actions/:id` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-an-action.md) for the provider-specific parameters and requirements.

