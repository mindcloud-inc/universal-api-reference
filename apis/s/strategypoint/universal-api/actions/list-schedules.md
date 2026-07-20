# Strategypoint: List Schedules

Retrieves schedules from Strategypoint.

```
GET https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strategypoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-schedules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strategypoint/latest/actions/list-schedules?${params}`, {
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
| `count` | number | no | Maximum number of records to return. |
| `lastEdited` | string | no | Filter by last-edited timestamp. |
| `lastEditedBy` | number | no | Filter by the user who last edited the record. |
| `order` | string | no | Sort order for the result set. |
| `page` | number | no | Page number to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "enabled": true,
      "lastRun": "string",
      "name": "Ava Chen",
      "nextRun": "string",
      "recurrence": "string",
      "scheduleId": 1,
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the schedule is active. |
| `enabled` | boolean | Whether the schedule is enabled. |
| `lastRun` | string | The last run timestamp. |
| `name` | string | The schedule name. |
| `nextRun` | string | The next scheduled run timestamp. |
| `recurrence` | string | The recurrence rule for the schedule. |
| `scheduleId` | number | The unique schedule identifier. |
| `state` | string | The current schedule state. |

## Native endpoint

Through the native Strategypoint API, this operation is `GET /schedules` (base URL `https://app.clearpointstrategy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-schedules.md) for the provider-specific parameters and requirements.

