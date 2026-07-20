# Boomlify: Get Dashboard Telegram Forwarding

Retrieves Telegram forwarding status for an owned mailbox in Boomlify.

```
GET https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-dashboard-telegram-forwarding
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Boomlify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-dashboard-telegram-forwarding?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boomlify/latest/actions/get-dashboard-telegram-forwarding?${params}`, {
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
| `id` | string | yes | Boomlify dashboard email UUID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "emailId": "ava@example.com",
      "id": "string",
      "isEnabled": true,
      "telegramChatId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `emailId` | string | Dashboard email identifier. |
| `id` | string | Telegram forwarding configuration identifier. |
| `isEnabled` | boolean | Whether Telegram forwarding is enabled. |
| `telegramChatId` | string | Telegram chat identifier when available. |

## Native endpoint

Through the native Boomlify API, this operation is `GET /api/v1/emails/{id}/telegram-forwarding` (base URL `https://v1.boomlify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dashboard-telegram-forwarding.md) for the provider-specific parameters and requirements.

