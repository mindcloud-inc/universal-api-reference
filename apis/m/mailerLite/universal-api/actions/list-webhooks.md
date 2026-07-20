# MailerLite: List Webhooks

Retrieves all webhook endpoints from MailerLite.

```
GET https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-webhooks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-webhooks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-webhooks?${params}`, {
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
      "batchable": true,
      "createdAt": "string",
      "enabled": true,
      "events": [
        "string"
      ],
      "id": "string",
      "isBlocked": true,
      "lastFiredAt": "string",
      "name": "Ava Chen",
      "responseCode": 1,
      "updatedAt": "string",
      "url": "https://example.com",
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `batchable` | boolean |  |
| `createdAt` | string |  |
| `enabled` | boolean |  |
| `events` | array<string> |  |
| `id` | string |  |
| `isBlocked` | boolean |  |
| `lastFiredAt` | string |  |
| `name` | string |  |
| `responseCode` | number |  |
| `updatedAt` | string |  |
| `url` | string |  |
| `version` | string |  |

## Native endpoint

Through the native MailerLite API, this operation is `GET /webhooks` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-webhooks.md) for the provider-specific parameters and requirements.

