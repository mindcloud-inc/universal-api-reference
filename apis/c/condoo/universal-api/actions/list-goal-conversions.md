# condoo: List Goal Conversions

Retrieves goal conversions from condoo.

```
GET https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-goal-conversions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a condoo `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-goal-conversions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/condoo/latest/actions/list-goal-conversions?${params}`, {
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
| `goalId` | number | no | Optional goal ID selector. |
| `websiteId` | number | no | Optional website ID selector. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datetime": "2026-05-07T12:00:00.000Z",
      "event_id": 1,
      "id": 1,
      "session_id": 1,
      "user_id": 1,
      "visitor_id": 1,
      "website_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datetime` | date |  |
| `event_id` | number |  |
| `id` | number |  |
| `session_id` | number |  |
| `user_id` | number |  |
| `visitor_id` | number |  |
| `website_id` | number |  |

## Native endpoint

Through the native condoo API, this operation is `GET /goals-conversions/` (base URL `https://trk.condoo.systems/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-goal-conversions.md) for the provider-specific parameters and requirements.

