# Fidel API: List Programs

Retrieves programs from Fidel API.

```
GET https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-programs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-programs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/list-programs?${params}`, {
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
      "accountId": "string",
      "active": true,
      "activeDate": "2026-05-07T12:00:00.000Z",
      "created": "2026-05-07T12:00:00.000Z",
      "icon": "string",
      "iconBackground": "string",
      "id": "string",
      "live": true,
      "name": "Ava Chen",
      "sync": true,
      "syncStats": {
        "status": "string"
      },
      "type": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `active` | boolean |  |
| `activeDate` | date |  |
| `created` | date |  |
| `icon` | string |  |
| `iconBackground` | string |  |
| `id` | string |  |
| `live` | boolean |  |
| `name` | string |  |
| `sync` | boolean |  |
| `syncStats.status` | string |  |
| `type` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Fidel API API, this operation is `GET /programs` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-programs.md) for the provider-specific parameters and requirements.

