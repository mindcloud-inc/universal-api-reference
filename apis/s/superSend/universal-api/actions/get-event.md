# SuperSend: Get Event

Retrieves an event from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-event
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-event?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-event?${params}`, {
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
| `id` | string | yes | Resource ID (UUID) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "autoresponse": true,
      "bounced": true,
      "campaign_id": "string",
      "campaign": {
        "id": "string",
        "name": "Ava Chen"
      },
      "channel": "string",
      "clicked": true,
      "clicks": 1,
      "contact_id": "string",
      "contact": {
        "email": "ava@example.com",
        "first_name": "Ava",
        "id": "string",
        "last_name": "Chen"
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "date": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "opened": true,
      "opens": 1,
      "replied": true,
      "replies": 1,
      "sender_id": "string",
      "sender": {
        "email": "ava@example.com",
        "id": "string",
        "send_as": "string"
      },
      "sequence_step": 1,
      "subject": "string",
      "type": "string",
      "unsubscribes": 1,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoresponse` | boolean |  |
| `bounced` | boolean |  |
| `campaign_id` | string |  |
| `campaign.id` | string |  |
| `campaign.name` | string |  |
| `channel` | string |  |
| `clicked` | boolean |  |
| `clicks` | number |  |
| `contact_id` | string |  |
| `contact.email` | string |  |
| `contact.first_name` | string |  |
| `contact.id` | string |  |
| `contact.last_name` | string |  |
| `created_at` | date |  |
| `date` | date |  |
| `id` | string |  |
| `opened` | boolean |  |
| `opens` | number |  |
| `replied` | boolean |  |
| `replies` | number |  |
| `sender_id` | string |  |
| `sender.email` | string |  |
| `sender.id` | string |  |
| `sender.send_as` | string |  |
| `sequence_step` | number |  |
| `subject` | string |  |
| `type` | string |  |
| `unsubscribes` | number |  |
| `updated_at` | date |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /events/{id}` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event.md) for the provider-specific parameters and requirements.

