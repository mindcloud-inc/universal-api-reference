# AssignX: Reset Conversation Context

Resets stored conversation context in AssignX.

```
DELETE https://connect.mindcloud.co/v1/universal/assignX/latest/actions/reset-conversation-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AssignX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/assignX/latest/actions/reset-conversation-context?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assignX/latest/actions/reset-conversation-context?${params}`, {
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
| `id` | string | yes | Conversation identifier whose memory context should be reset. |

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
| `success` | boolean |  |

## Native endpoint

Through the native AssignX API, this operation is `DELETE conversations/:id` (base URL `https://api.agentx.so/api/v1/access/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/reset-conversation-context.md) for the provider-specific parameters and requirements.

