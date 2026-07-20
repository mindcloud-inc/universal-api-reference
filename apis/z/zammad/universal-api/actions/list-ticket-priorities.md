# Zammad: List Ticket Priorities

Retrieves ticket priorities from Zammad.

```
GET https://connect.mindcloud.co/v1/universal/zammad/latest/actions/list-ticket-priorities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zammad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zammad/latest/actions/list-ticket-priorities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zammad/latest/actions/list-ticket-priorities?${params}`, {
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
      "active": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "defaultCreate": true,
      "id": 1,
      "name": "Ava Chen",
      "uiColor": "string",
      "uiIcon": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdAt` | date |  |
| `defaultCreate` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `uiColor` | string |  |
| `uiIcon` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Zammad API, this operation is `GET /ticket_priorities` (base URL `{{credentials.baseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-ticket-priorities.md) for the provider-specific parameters and requirements.

