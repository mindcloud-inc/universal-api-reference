# Beyond Presence: List Call Messages

Retrieves transcribed messages from a Beyond Presence call.

```
GET https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/list-call-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Beyond Presence `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/list-call-messages?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beyondPresence/latest/actions/list-call-messages?${params}`, {
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
| `id` | string | yes | Call ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "sender": "string",
      "sentAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Message text content. |
| `sender` | string | Message sender. |
| `sentAt` | date | Sent time in ISO 8601 format. |

## Native endpoint

Through the native Beyond Presence API, this operation is `GET /v1/calls/:id/messages` (base URL `https://api.bey.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-call-messages.md) for the provider-specific parameters and requirements.

