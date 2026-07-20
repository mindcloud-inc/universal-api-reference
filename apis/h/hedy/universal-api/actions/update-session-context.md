# Hedy: Update Session Context

Updates an existing session context in Hedy.

```
PUT https://connect.mindcloud.co/v1/universal/hedy/latest/actions/update-session-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hedy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/hedy/latest/actions/update-session-context" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contextId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hedy/latest/actions/update-session-context', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contextId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | no | New content for the session context. |
| `contextId` | string | yes | Unique identifier of the session context. |
| `isDefault` | boolean | no | Set as the default context. |
| `title` | string | no | New title for the session context. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isDefault": true,
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `createdAt` | date |  |
| `id` | string |  |
| `isDefault` | boolean |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Hedy API, this operation is `PATCH https://api.hedy.bot/contexts/:contextId` (base URL `https://api.hedy.bot`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-session-context.md) for the provider-specific parameters and requirements.

