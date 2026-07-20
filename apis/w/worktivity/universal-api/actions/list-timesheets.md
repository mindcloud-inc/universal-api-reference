# Worktivity: List Timesheets

Retrieves timesheets from Worktivity with date filters.

```
GET https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-timesheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worktivity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-timesheets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-timesheets?${params}`, {
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
      "activityLevel": 1,
      "clockIn": "2026-05-07T12:00:00.000Z",
      "clockOut": "2026-05-07T12:00:00.000Z",
      "employee": {},
      "id": "string",
      "idle": 1,
      "natural": 1,
      "onBreak": 1,
      "productive": 1,
      "productivity": 1,
      "status": 1,
      "totalMins": 1,
      "unproductive": 1,
      "working": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityLevel` | number |  |
| `clockIn` | date |  |
| `clockOut` | date |  |
| `employee` | object |  |
| `id` | string |  |
| `idle` | number |  |
| `natural` | number |  |
| `onBreak` | number |  |
| `productive` | number |  |
| `productivity` | number |  |
| `status` | number |  |
| `totalMins` | number |  |
| `unproductive` | number |  |
| `working` | number |  |

## Native endpoint

Through the native Worktivity API, this operation is `POST /Timesheet/List` (base URL `https://open-api.useworktivity.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-timesheets.md) for the provider-specific parameters and requirements.

