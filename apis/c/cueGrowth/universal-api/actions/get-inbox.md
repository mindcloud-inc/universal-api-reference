# CueGrowth: Get Inbox



```
GET https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/get-inbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CueGrowth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/get-inbox?connectionId=$CONNECTION_ID&inboxId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "inboxId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/get-inbox?${params}`, {
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
| `inboxId` | string | yes | ID of the inbox. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {
        "id": 1,
        "name": "Ava Chen",
        "type": "string"
      },
      "conversation": [
        {
          "inbox": "string",
          "linkedin_id": "https://example.com",
          "message": "string",
          "sender": "string",
          "sent_date": "string"
        }
      ],
      "creation_date": "string",
      "is_connected": true,
      "last_message_date": "string",
      "receiver": {
        "email": "ava@example.com",
        "first_name": "Ava",
        "id": 1,
        "last_name": "Chen",
        "linkedin_url": "https://example.com",
        "username": "Ava Chen"
      },
      "update_date": "string",
      "user": {
        "email": "ava@example.com",
        "id": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign.id` | number |  |
| `campaign.name` | string |  |
| `campaign.type` | string |  |
| `conversation[].inbox` | string |  |
| `conversation[].linkedin_id` | string |  |
| `conversation[].message` | string |  |
| `conversation[].sender` | string |  |
| `conversation[].sent_date` | string |  |
| `creation_date` | string |  |
| `is_connected` | boolean |  |
| `last_message_date` | string |  |
| `receiver.email` | string |  |
| `receiver.first_name` | string |  |
| `receiver.id` | number |  |
| `receiver.last_name` | string |  |
| `receiver.linkedin_url` | string |  |
| `receiver.username` | string |  |
| `update_date` | string |  |
| `user.email` | string |  |
| `user.id` | number |  |

## Native endpoint

Through the native CueGrowth API, this operation is `GET /inbox/{inbox_id}` (base URL `https://api.cuegrowth.ai/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-inbox.md) for the provider-specific parameters and requirements.

