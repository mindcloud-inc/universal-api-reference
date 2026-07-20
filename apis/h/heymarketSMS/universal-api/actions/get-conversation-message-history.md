# Heymarket SMS: Get Conversation Message History



```
GET https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-conversation-message-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-conversation-message-history?connectionId=$CONNECTION_ID&phoneNumber=15555550123&inboxId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "phoneNumber": "15555550123",
  "inboxId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-conversation-message-history?${params}`, {
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
| `phoneNumber` | string | yes | Target phone number in E.164 format without the plus sign. Example: `15555550123`. |
| `inboxId` | number | yes | Unique identifier of the inbox. |
| `timestamp` | number | no | Latest time to search as a Unix timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "channel": "string",
      "conversation": {},
      "date": "2026-05-07T12:00:00.000Z",
      "hidden": true,
      "id": 1,
      "local_id": "string",
      "raw_error": "string",
      "status": "string",
      "super": 1,
      "target": "string",
      "target_errors": {},
      "text": "string",
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z",
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `channel` | string |  |
| `conversation` | object |  |
| `date` | date |  |
| `hidden` | boolean |  |
| `id` | number |  |
| `local_id` | string |  |
| `raw_error` | string |  |
| `status` | string |  |
| `super` | number |  |
| `target` | string |  |
| `target_errors` | object |  |
| `text` | string |  |
| `type` | string |  |
| `updated` | date |  |
| `user` | number |  |

## Native endpoint

Through the native Heymarket SMS API, this operation is `GET /v1/messages` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-conversation-message-history.md) for the provider-specific parameters and requirements.

