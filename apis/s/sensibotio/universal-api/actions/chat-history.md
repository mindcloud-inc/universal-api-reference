# Sensibot.io: Chat History

Retrieves chat history for a recipient from Sensibot.io.

```
GET https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/chat-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sensibot.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/chat-history?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sensibotio/latest/actions/chat-history?${params}`, {
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
| `recipient` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        [
          {}
        ]
      ],
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[]` | array<object> |  |
| `message` | string |  |
| `status` | number |  |

## Native endpoint

Through the native Sensibot.io API, this operation is `POST /assistant/chathistory` (base URL `https://api.sensibot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/chat-history.md) for the provider-specific parameters and requirements.

