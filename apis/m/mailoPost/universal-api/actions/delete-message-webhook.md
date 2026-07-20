# MailoPost: Delete Message Webhook

Deletes an existing message webhook from MailoPost.

```
DELETE https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/delete-message-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailoPost `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/delete-message-webhook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/delete-message-webhook?${params}`, {
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
| `id` | string | yes | MailoPost message webhook identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        "string"
      ],
      "id": 1,
      "kinds": [
        "string"
      ],
      "status": "string",
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events[]` | string |  |
| `id` | number |  |
| `kinds[]` | string |  |
| `status` | string |  |
| `title` | string |  |
| `url` | string |  |

## Native endpoint

Through the native MailoPost API, this operation is `DELETE /email/messages_webhooks/:id` (base URL `https://api.mailopost.ru/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-message-webhook.md) for the provider-specific parameters and requirements.

