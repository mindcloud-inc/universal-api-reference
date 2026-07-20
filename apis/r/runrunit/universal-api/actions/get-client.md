# Runrun.it: Get Client

Retrieves a client from Runrun.it.

```
GET https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Runrun.it `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/get-client?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/runrunit/latest/actions/get-client?${params}`, {
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
| `id` | string | yes | Id path parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activities": 1,
      "activities_0_days_ago": 1,
      "activities_1_days_ago": 1,
      "activities_2_days_ago": 1,
      "activities_3_days_ago": 1,
      "activities_4_days_ago": 1,
      "activities_5_days_ago": 1,
      "activities_6_days_ago": 1,
      "budgeted_cost_month": 1,
      "budgeted_hours_month": 1,
      "cost_pending": 1,
      "cost_total": 1,
      "cost_worked": 1,
      "custom_field": "string",
      "id": 1,
      "is_visible": true,
      "name": "Ava Chen",
      "project_groups": [
        "string"
      ],
      "projects_count": 1,
      "time_pending": 1,
      "time_pending_backlog": 1,
      "time_pending_not_assigned": 1,
      "time_pending_queued": 1,
      "time_progress": 1,
      "time_total": 1,
      "time_worked": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activities` | number | Total time (in seconds) worked today and in the last 6 days |
| `activities_0_days_ago` | number | Time (in seconds) worked in the client today |
| `activities_1_days_ago` | number | Time (in seconds) worked in the client 1 days ago |
| `activities_2_days_ago` | number | Time (in seconds) worked in the client 2 days ago |
| `activities_3_days_ago` | number | Time (in seconds) worked in the client 3 days ago |
| `activities_4_days_ago` | number | Time (in seconds) worked in the client 4 days ago |
| `activities_5_days_ago` | number | Time (in seconds) worked in the client 5 days ago |
| `activities_6_days_ago` | number | Time (in seconds) worked in the client 6 days ago |
| `budgeted_cost_month` | number | Budgeted cost per month |
| `budgeted_hours_month` | number | Budgeted hours per month |
| `cost_pending` | number | Cost pending in the client |
| `cost_total` | number | Total cost of the client |
| `cost_worked` | number | Cost spent on the client |
| `custom_field` | string | Custom field |
| `id` | number | Client ID |
| `is_visible` | boolean | Client is currently visible to be used |
| `name` | string | Client's name |
| `project_groups` | array<string> | [Deprecated] Not used anymore |
| `projects_count` | number | Number of projects in the client |
| `time_pending` | number | Time (in seconds) pending in the client |
| `time_pending_backlog` | number | [Deprecated] Use 'time_pending_not_assigned' instead |
| `time_pending_not_assigned` | number | Time (in seconds) pending not assigned in the client |
| `time_pending_queued` | number | Time (in seconds) pending queued in the client |
| `time_progress` | number | Progress of time worked on the client |
| `time_total` | number | Total time (in seconds) spent in the client |
| `time_worked` | number | Time (in seconds) worked in the client |

## Native endpoint

Through the native Runrun.it API, this operation is `GET /clients/:id` (base URL `https://runrun.it/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

