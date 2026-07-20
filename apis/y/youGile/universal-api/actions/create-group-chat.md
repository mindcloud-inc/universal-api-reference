# YouGile: Create group chat

Creates a new group chat in YouGile.

```
POST https://connect.mindcloud.co/v1/universal/youGile/latest/actions/create-group-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouGile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/youGile/latest/actions/create-group-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "string",
  "users": {},
  "userRoleMap": {},
  "roleConfigMap": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youGile/latest/actions/create-group-chat', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "string",
    "users": {},
    "userRoleMap": {},
    "roleConfigMap": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | The group chat title. |
| `users` | object | yes | Map of chat users and notification settings. |
| `userRoleMap` | object | yes | Map of user IDs to chat roles. |
| `roleConfigMap` | object | yes | Role configuration map for the chat. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native YouGile API, this operation is `POST /group-chats` (base URL `{{credentials.companyDomain}}/api-v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-group-chat.md) for the provider-specific parameters and requirements.

