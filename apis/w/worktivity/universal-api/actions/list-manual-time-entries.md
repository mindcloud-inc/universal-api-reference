# Worktivity: List Manual Time Entries

Retrieves manual time entries from Worktivity.

```
GET https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-manual-time-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Worktivity `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-manual-time-entries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/worktivity/latest/actions/list-manual-time-entries?${params}`, {
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
      "employee": {},
      "employeeId": "string",
      "endDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "logStatus": 1,
      "productivityStatus": 1,
      "projectId": "string",
      "projectTaskId": "string",
      "reason": "string",
      "startDate": "2026-05-07T12:00:00.000Z",
      "status": 1,
      "totalMinutes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `employee` | object |  |
| `employeeId` | string |  |
| `endDate` | date |  |
| `id` | string |  |
| `logStatus` | number |  |
| `productivityStatus` | number |  |
| `projectId` | string |  |
| `projectTaskId` | string |  |
| `reason` | string |  |
| `startDate` | date |  |
| `status` | number |  |
| `totalMinutes` | number |  |

## Native endpoint

Through the native Worktivity API, this operation is `POST /TimeEntry/List` (base URL `https://open-api.useworktivity.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-manual-time-entries.md) for the provider-specific parameters and requirements.

