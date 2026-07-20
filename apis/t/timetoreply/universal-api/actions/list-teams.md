# Timetoreply: List Teams



```
GET https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-teams
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timetoreply `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-teams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timetoreply/latest/actions/list-teams?${params}`, {
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
| `includeEmails` | boolean | no | Include team email addresses in the response. |
| `search` | string | no | Filter teams by a search term. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agents_count": 1,
      "company_id": 1,
      "created_at": "string",
      "first_reply_time_goal": 1,
      "id": 1,
      "model_type": "string",
      "name": "Ava Chen",
      "overall_reply_time_goal": 1,
      "time_to_close_goal": 1,
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agents_count` | number |  |
| `company_id` | number |  |
| `created_at` | string |  |
| `first_reply_time_goal` | number |  |
| `id` | number |  |
| `model_type` | string |  |
| `name` | string |  |
| `overall_reply_time_goal` | number |  |
| `time_to_close_goal` | number |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Timetoreply API, this operation is `GET /api/entities/teams` (base URL `https://portal.timetoreply.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-teams.md) for the provider-specific parameters and requirements.

