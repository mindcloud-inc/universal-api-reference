# Rentman: List Crew Rates



```
GET https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-crew-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-crew-rates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-crew-rates?${params}`, {
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
      "archived": true,
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "displayname": "Ava Chen",
      "id": 1,
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "subtype": "string",
      "type": "string",
      "updateHash": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `created` | date |  |
| `creator` | string |  |
| `displayname` | string |  |
| `id` | number |  |
| `modified` | date |  |
| `name` | string |  |
| `subtype` | string |  |
| `type` | string |  |
| `updateHash` | string |  |

## Native endpoint

Through the native Rentman API, this operation is `GET /rates` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-crew-rates.md) for the provider-specific parameters and requirements.

