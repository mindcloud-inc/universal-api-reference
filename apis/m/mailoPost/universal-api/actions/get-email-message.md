# MailoPost: Get Email Message

Retrieves an email message from MailoPost.

```
GET https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-email-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-email-message?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-email-message?${params}`, {
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
| `id` | string | yes | MailoPost message identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": {
        "open": 1,
        "spam": 1,
        "unsubscribe": 1
      },
      "from_email": "ava@example.com",
      "from_name": "Ava Chen",
      "html": "string",
      "id": 1,
      "status": "string",
      "subject": "string",
      "text": "string",
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events.open` | number |  |
| `events.spam` | number |  |
| `events.unsubscribe` | number |  |
| `from_email` | string |  |
| `from_name` | string |  |
| `html` | string |  |
| `id` | number |  |
| `status` | string |  |
| `subject` | string |  |
| `text` | string |  |
| `to` | string |  |

## Native endpoint

Through the native MailoPost API, this operation is `GET /email/messages/:id` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-message.md) for the provider-specific parameters and requirements.

