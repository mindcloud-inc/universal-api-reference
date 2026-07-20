# Moderation API: Get An Action

Retrieves a moderation action from Moderation API.

```
GET https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-an-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-an-action?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-an-action?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the action to get. |

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

Through the native Moderation API API, this operation is `GET /actions/:id` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-an-action.md) for the provider-specific parameters and requirements.

