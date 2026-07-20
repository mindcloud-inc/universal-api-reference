# SuperSend: List Webhooks

Retrieves webhooks from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-webhooks?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/list-webhooks?${params}`, {
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
| `teamId` | string | yes |  |
| `enabled` | boolean | no |  |
| `limit` | number | no | Default: 50. Range: 1 to 100. |
| `offset` | number | no | Default: 0. Range: 0 to inf. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign_count": 1,
      "config": {
        "bounce_event": true,
        "click_event": true,
        "open_event": true,
        "reply_event": true,
        "sent_event": true,
        "unsubscribe_event": true
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "enabled": true,
      "id": "string",
      "name": "Ava Chen",
      "object": "string",
      "secret": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_count` | number |  |
| `config.bounce_event` | boolean |  |
| `config.click_event` | boolean |  |
| `config.open_event` | boolean |  |
| `config.reply_event` | boolean |  |
| `config.sent_event` | boolean |  |
| `config.unsubscribe_event` | boolean |  |
| `created_at` | date |  |
| `enabled` | boolean |  |
| `id` | string |  |
| `name` | string |  |
| `object` | string |  |
| `secret` | string |  |
| `updated_at` | date |  |
| `url` | string |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /webhooks` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

