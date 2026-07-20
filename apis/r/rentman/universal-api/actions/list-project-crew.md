# Rentman: List Project Crew



```
GET https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-project-crew
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rentman `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-project-crew?connectionId=$CONNECTION_ID&limit=25&offset=0&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-project-crew?${params}`, {
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
| `id` | number | yes | Numeric Rentman project identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activity_status": "string",
      "cost_accommodation": 1,
      "cost_actual": 1,
      "cost_catering": 1,
      "cost_other": 1,
      "cost_planned": 1,
      "cost_rate": "string",
      "cost_travel": 1,
      "costs": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "creator": "string",
      "crewmember": "string",
      "custom": {},
      "diff_cost": 1,
      "diff_hours": 1,
      "displayname": "Ava Chen",
      "function": "string",
      "hours_planned": 1,
      "hours_registered": 1,
      "id": 1,
      "invoice_reference": "string",
      "is_visible_on_dashboard": true,
      "modified": "2026-05-07T12:00:00.000Z",
      "planperiod_end": "2026-05-07T12:00:00.000Z",
      "planperiod_start": "2026-05-07T12:00:00.000Z",
      "project_leader": true,
      "remark": "string",
      "remark_planner": "string",
      "transport": "string",
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activity_status` | string |  |
| `cost_accommodation` | number |  |
| `cost_actual` | number |  |
| `cost_catering` | number |  |
| `cost_other` | number |  |
| `cost_planned` | number |  |
| `cost_rate` | string |  |
| `cost_travel` | number |  |
| `costs` | number |  |
| `created` | date |  |
| `creator` | string |  |
| `crewmember` | string |  |
| `custom` | object |  |
| `diff_cost` | number |  |
| `diff_hours` | number |  |
| `displayname` | string |  |
| `function` | string |  |
| `hours_planned` | number |  |
| `hours_registered` | number |  |
| `id` | number |  |
| `invoice_reference` | string |  |
| `is_visible_on_dashboard` | boolean |  |
| `modified` | date |  |
| `planperiod_end` | date |  |
| `planperiod_start` | date |  |
| `project_leader` | boolean |  |
| `remark` | string |  |
| `remark_planner` | string |  |
| `transport` | string |  |
| `visible` | boolean |  |

## Native endpoint

Through the native Rentman API, this operation is `GET /projects/:id/projectcrew` (base URL `https://api.rentman.net`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-project-crew.md) for the provider-specific parameters and requirements.

