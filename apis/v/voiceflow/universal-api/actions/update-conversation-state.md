# Voiceflow: Update Conversation State

Updates a user's conversation state in Voiceflow.

```
PUT https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/update-conversation-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/update-conversation-state" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "wizard-stage3-user-state",
  "state": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/update-conversation-state', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "wizard-stage3-user-state",
    "state": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | ID of the user whose conversation state should be replaced. Example: `wizard-stage3-user-state`. |
| `state` | object | yes | Full conversation state object with stack, variables, storage, and turn. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voiceflow API returns.

## Native endpoint

Through the native Voiceflow API, this operation is `PUT /state/user/:userId` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-conversation-state.md) for the provider-specific parameters and requirements.

