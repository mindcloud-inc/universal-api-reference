# TimelinesAI: List Chats

Retrieves chats from your TimelinesAI workspace.

```
GET https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-chats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TimelinesAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-chats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timelinesAI/latest/actions/list-chats?${params}`, {
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
| `label` | string | no | Filter chats by label. Use a comma-separated list to match any listed label. |
| `whatsappAccountId` | string | no | Filter chats by one or more WhatsApp account IDs in wid format. |
| `group` | boolean | no | Filter for group chats or direct chats. |
| `responsible` | string | no | Filter chats assigned to specific users by email address. Use commas for multiple values. |
| `name` | string | no | Filter chats whose name contains one or more strings. Use commas for multiple values. |
| `phone` | string | no | Filter direct chats by a phone number. |
| `read` | boolean | no | Filter for read or unread chats. |
| `closed` | boolean | no | Filter for closed or open chats. |
| `chatgptAutoresponseEnabled` | boolean | no | Filter chats where ChatGPT auto-response is enabled or disabled. |
| `page` | number | no | Page number starting at 1. |
| `createdAfter` | date | no | Filter chats created after this timestamp. |
| `createdBefore` | date | no | Filter chats created before this timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "chats": [
          {
            "closed": true,
            "id": 1,
            "isGroup": true,
            "jid": "string",
            "labels": [
              "string"
            ],
            "name": "Ava Chen",
            "phone": "string",
            "read": true
          }
        ],
        "hasMorePages": true
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `data.chats` | array<object> |  |
| `data.chats[].closed` | boolean |  |
| `data.chats[].id` | number |  |
| `data.chats[].isGroup` | boolean |  |
| `data.chats[].jid` | string |  |
| `data.chats[].labels` | array<string> |  |
| `data.chats[].name` | string |  |
| `data.chats[].phone` | string |  |
| `data.chats[].read` | boolean |  |
| `data.hasMorePages` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native TimelinesAI API, this operation is `GET /chats` (base URL `https://app.timelines.ai/integrations/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chats.md) for the provider-specific parameters and requirements.

