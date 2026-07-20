# Boost: List Automation Triggers

Retrieves automation trigger records from Boost.

```
GET https://connect.mindcloud.co/v1/universal/boost/latest/actions/list-automation-triggers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Boost `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boost/latest/actions/list-automation-triggers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boost/latest/actions/list-automation-triggers?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "name": "Ava Chen",
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
| `created` | date | Creation timestamp. |
| `id` | number | Trigger ID. |
| `name` | string | Trigger name. |
| `type` | string | Trigger type. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Boost API, this operation is `GET /automatization/trigger` (base URL `https://{{credentials.systemKey}}.boost.space/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-automation-triggers.md) for the provider-specific parameters and requirements.

