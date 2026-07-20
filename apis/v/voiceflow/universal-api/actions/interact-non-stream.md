# Voiceflow: Interact Non-Stream

Sends a conversation action to Voiceflow and returns traces.

```
POST https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/interact-non-stream
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voiceflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/interact-non-stream" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "mindcloud-voiceflow-user-001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voiceflow/latest/actions/interact-non-stream', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "mindcloud-voiceflow-user-001"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | string | yes | An ID which uniquely identifies the user having the conversation. Example: `mindcloud-voiceflow-user-001`. |
| `request` | object | no | The user's request payload. Example: `[object Object]`. |
| `action` | object | no | The action payload used to launch or control the interaction. Example: `[object Object]`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `state` | object | no | Optional conversation state payload. Example: `[object Object]`. |
| `config` | object | no | Optional settings to configure the response. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voiceflow API returns.

## Native endpoint

Through the native Voiceflow API, this operation is `POST /state/user/:userId/interact` (base URL `https://general-runtime.voiceflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/interact-non-stream.md) for the provider-specific parameters and requirements.

