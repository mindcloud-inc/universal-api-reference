# Timely: List Task Summaries

Retrieves task summaries from Timely.

```
GET https://connect.mindcloud.co/v1/universal/timely/latest/actions/list-task-summaries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timely/latest/actions/list-task-summaries?connectionId=$CONNECTION_ID&accountId=1&resource=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "1",
  "resource": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timely/latest/actions/list-task-summaries?${params}`, {
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
| `accountId` | number | yes | Account ID |
| `resource` | string | yes | Resource type to group summaries by |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `since` | date | no | Filter tasks from this date |
| `until` | date | no | Filter tasks up to this date |
| `completed` | string | no | Filter by completion status |
| `userIds` | string | no | Comma-separated user IDs to filter by |
| `projectIds` | string | no | Comma-separated project IDs to filter by |
| `forecastIds` | string | no | Comma-separated task IDs to filter by |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Timely API returns.

## Native endpoint

Through the native Timely API, this operation is `GET /1.1/{account_id}/forecasts/{resource}/summary` (base URL `https://api.timelyapp.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-summaries.md) for the provider-specific parameters and requirements.

