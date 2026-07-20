# Moderation API: Execute Moderation Action

Executes a moderation action in Moderation API.

```
POST https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/execute-moderation-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/execute-moderation-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actionKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/execute-moderation-action', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actionKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actionKey` | string | yes | ID or key of the action to execute |
| `value` | string | no | Optional value to provide with the action |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contentIds[]` | array<string> | no | IDs of the content items to apply the action to. Provide this or authorIds. |
| `authorIds[]` | array<string> | no | IDs of the authors to apply the action to. Provide this or contentIds. |
| `queueId` | string | no | Optional queue ID if the action is queue-specific |
| `duration` | number | no | Optional duration in milliseconds for actions with timeouts |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the action was executed successfully |

## Native endpoint

Through the native Moderation API API, this operation is `POST /actions/execute` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-moderation-action.md) for the provider-specific parameters and requirements.

