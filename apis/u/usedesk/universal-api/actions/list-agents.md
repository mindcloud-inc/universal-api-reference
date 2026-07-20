# Usedesk: List Agents

Retrieves a list of agents from Usedesk.

```
GET https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-agents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Usedesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-agents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-agents?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "chat_online_status": 1,
      "email": "ava@example.com",
      "groups": [
        {}
      ],
      "id": 1,
      "name": "Ava Chen",
      "online_status": 1,
      "phone": "string",
      "position": "string",
      "role": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `chat_online_status` | number |  |
| `email` | string |  |
| `groups` | array<object> |  |
| `id` | number |  |
| `name` | string |  |
| `online_status` | number |  |
| `phone` | string |  |
| `position` | string |  |
| `role` | string |  |

## Native endpoint

Through the native Usedesk API, this operation is `POST /users` (base URL `https://secure.usedesk.com/uapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-agents.md) for the provider-specific parameters and requirements.

