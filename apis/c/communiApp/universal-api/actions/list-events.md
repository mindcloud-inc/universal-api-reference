# Communi App: List Events



```
GET https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Communi App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-events?connectionId=$CONNECTION_ID&group=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/communiApp/latest/actions/list-events?${params}`, {
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
| `group` | number | yes | The CommuniApp group ID. The endpoint requires a group context for event listings. |
| `search` | string | no | Optional full-text search across event title, description, and location. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_loadStatus": 1,
      "_rls": 1,
      "communiApp": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "group": 1,
      "id": 1,
      "messageFormatted": "string",
      "titleFormatted": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_loadStatus` | number |  |
| `_rls` | number |  |
| `communiApp` | number |  |
| `createdOn` | date |  |
| `group` | number |  |
| `id` | number |  |
| `messageFormatted` | string |  |
| `titleFormatted` | string |  |
| `updatedOn` | date |  |

## Native endpoint

Through the native Communi App API, this operation is `GET /rest/event` (base URL `https://api.communiapp.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-events.md) for the provider-specific parameters and requirements.

