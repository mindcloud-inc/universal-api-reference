# Das Keyboard 5Q: List Signals

Retrieves signals from Das Keyboard 5Q.

```
GET https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/list-signals
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Das Keyboard 5Q `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/list-signals?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dasKeyboard5Q/latest/actions/list-signals?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sort` | string | no | Sort expression for signals. The docs show createdAt,DESC or createdAt,ASC. Default: `createdAt,DESC`. Example: `createdAt,DESC`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientName": "Ava Chen",
      "color": "string",
      "createdAt": 1,
      "effect": "string",
      "id": 1,
      "isArchived": true,
      "isMuted": true,
      "isRead": true,
      "message": "string",
      "name": "Ava Chen",
      "pid": "string",
      "updatedAt": 1,
      "userId": 1,
      "zoneId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientName` | string | Client that created the signal. |
| `color` | string | Signal color. |
| `createdAt` | number | Creation timestamp in milliseconds. |
| `effect` | string | Signal visual effect. |
| `id` | number | Signal ID. |
| `isArchived` | boolean | Whether the signal is archived. |
| `isMuted` | boolean | Whether the signal is muted in the API response. |
| `isRead` | boolean | Whether the signal is read. |
| `message` | string | Signal message. |
| `name` | string | Signal name. |
| `pid` | string | Device PID. |
| `updatedAt` | number | Update timestamp in milliseconds. |
| `userId` | number | Q Cloud user ID. |
| `zoneId` | string | Keyboard zone ID. |

## Native endpoint

Through the native Das Keyboard 5Q API, this operation is `GET /signals` (base URL `https://q2.daskeyboard.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-signals.md) for the provider-specific parameters and requirements.

