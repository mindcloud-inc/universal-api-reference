# Voiceflow: Get Conversation State

Retrieves a user's conversation state from Voiceflow.

```
GET https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-conversation-state
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-conversation-state?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/get-conversation-state?${params}`, {
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
| `userId` | string | yes | Unique ID of the user whose conversation state you want to fetch. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voiceflow API returns.

## Native endpoint

Through the native Voiceflow API, this operation is `GET /state/user/:userId` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation-state.md) for the provider-specific parameters and requirements.

