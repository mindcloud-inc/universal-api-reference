# Bulldog-WP: Search chat messages

Finds chat messages in Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-chat-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-chat-messages?connectionId=$CONNECTION_ID&limit=25&offset=0&deviceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "deviceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-chat-messages?${params}`, {
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
| `deviceId` | string | yes | WhatsApp number device ID from Bulldog WP. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agent": {},
      "chat": {},
      "chatWid": "string",
      "device": {},
      "flow": "string",
      "from": "string",
      "mtype": "string",
      "params": {},
      "reference": "string",
      "trigger": "string",
      "wid": "string",
      "widFull": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agent` | object |  |
| `chat` | object |  |
| `chatWid` | string |  |
| `device` | object |  |
| `flow` | string |  |
| `from` | string |  |
| `mtype` | string |  |
| `params` | object |  |
| `reference` | string |  |
| `trigger` | string |  |
| `wid` | string |  |
| `widFull` | string |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /chat/{deviceId}/messages` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-chat-messages.md) for the provider-specific parameters and requirements.

