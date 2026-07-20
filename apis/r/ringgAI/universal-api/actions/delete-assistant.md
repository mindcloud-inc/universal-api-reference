# Ringg AI: Delete Assistant

Archives an assistant in Ringg AI.

```
DELETE https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/delete-assistant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/delete-assistant?connectionId=$CONNECTION_ID&agentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/delete-assistant?${params}`, {
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
| `agentId` | string | yes | (Required) ID of the assistant to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Ringg AI API, this operation is `DELETE /agent/:agent_id` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-assistant.md) for the provider-specific parameters and requirements.

