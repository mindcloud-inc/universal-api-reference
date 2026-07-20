# Bulldog-WP: Get campaigns

Retrieves campaigns from Bulldog-WP.

```
GET https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bulldog-WP `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-campaigns?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bulldogWP/latest/actions/get-campaigns?${params}`, {
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
      "canceledAt": "2026-05-07T12:00:00.000Z",
      "clone": {},
      "completedAt": "2026-05-07T12:00:00.000Z",
      "device": {},
      "id": "string",
      "mode": "string",
      "name": "Ava Chen",
      "owner": {},
      "source": "string",
      "startedAt": "2026-05-07T12:00:00.000Z",
      "stoppedAt": "2026-05-07T12:00:00.000Z",
      "user": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `canceledAt` | date |  |
| `clone` | object |  |
| `completedAt` | date |  |
| `device` | object |  |
| `id` | string |  |
| `mode` | string |  |
| `name` | string |  |
| `owner` | object |  |
| `source` | string |  |
| `startedAt` | date |  |
| `stoppedAt` | date |  |
| `user` | object |  |

## Native endpoint

Through the native Bulldog-WP API, this operation is `GET /campaigns` (base URL `https://api.bulldog-wp.co.il/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-campaigns.md) for the provider-specific parameters and requirements.

