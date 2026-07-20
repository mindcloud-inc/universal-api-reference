# Hedy: Delete Session Context

Deletes a session context from Hedy.

```
DELETE https://connect.mindcloud.co/v1/universal/hedy/latest/actions/delete-session-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hedy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hedy/latest/actions/delete-session-context?connectionId=$CONNECTION_ID&contextId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contextId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hedy/latest/actions/delete-session-context?${params}`, {
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
| `contextId` | string | yes | Unique identifier of the session context. |

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

Through the native Hedy API, this operation is `DELETE https://api.hedy.bot/contexts/:contextId` (base URL `https://api.hedy.bot`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-session-context.md) for the provider-specific parameters and requirements.

