# YouGile: Update group chat

Updates an existing group chat in YouGile.

```
PUT https://connect.mindcloud.co/v1/universal/youGile/latest/actions/update-group-chat
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouGile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/youGile/latest/actions/update-group-chat" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youGile/latest/actions/update-group-chat', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The YouGile group chat ID. |
| `title` | string | no | The updated group chat title. |
| `users` | object | no | Updated map of chat users and notification settings. |
| `userRoleMap` | object | no | Updated map of user IDs to chat roles. |
| `roleConfigMap` | object | no | Updated role configuration map for the chat. |
| `deleted` | boolean | no | Mark the group chat as deleted. |

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

Through the native YouGile API, this operation is `PUT /group-chats/:id` (base URL `{{credentials.companyDomain}}/api-v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-group-chat.md) for the provider-specific parameters and requirements.

