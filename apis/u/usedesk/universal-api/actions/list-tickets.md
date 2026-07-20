# Usedesk: List Tickets

Retrieves a list of tickets from Usedesk.

```
GET https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-tickets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Usedesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-tickets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/usedesk/latest/actions/list-tickets?${params}`, {
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
      "assignee_id": 1,
      "channel_email": "ava@example.com",
      "channel_id": 1,
      "client_id": 1,
      "client_name": "Ava Chen",
      "created_at": "string",
      "group": 1,
      "id": 1,
      "last_comment": "string",
      "last_updated_at": "string",
      "priority": "string",
      "remind_at": "string",
      "status": 1,
      "subject": "string",
      "tags": [
        {}
      ],
      "ticket_fields": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignee_id` | number |  |
| `channel_email` | string |  |
| `channel_id` | number |  |
| `client_id` | number |  |
| `client_name` | string |  |
| `created_at` | string |  |
| `group` | number |  |
| `id` | number |  |
| `last_comment` | string |  |
| `last_updated_at` | string |  |
| `priority` | string |  |
| `remind_at` | string |  |
| `status` | number |  |
| `subject` | string |  |
| `tags` | array<object> |  |
| `ticket_fields` | array<object> |  |
| `type` | string |  |

## Native endpoint

Through the native Usedesk API, this operation is `POST /tickets` (base URL `https://secure.usedesk.com/uapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tickets.md) for the provider-specific parameters and requirements.

