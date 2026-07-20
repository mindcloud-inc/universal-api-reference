# actiTIME: Get Leave Time

Retrieves leave time records from actiTIME by date range.

```
GET https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-leave-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a actiTIME `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-leave-time?connectionId=$CONNECTION_ID&dateFrom=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "dateFrom": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/actiTIME/latest/actions/get-leave-time?${params}`, {
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
| `dateFrom` | string | yes | Start date of requested leave time in YYYY-MM-DD format. |
| `dateTo` | string | no | End date of requested leave time in YYYY-MM-DD format. |
| `includeReferenced` | string | no | Comma-separated referenced objects to include. |
| `leaveTypeIds` | string | no | Comma-separated leave type ids. |
| `stopAfter` | number | no | Approximate number of leave time records to return. |
| `userIds` | string | no | Comma-separated user ids. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "dayOffset": 1,
      "leaveTime": 1,
      "leaveTypeId": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | Leave date. |
| `dayOffset` | number | Offset in days from the requested start date. |
| `leaveTime` | number | Leave duration in minutes. |
| `leaveTypeId` | number | Leave type identifier. |
| `userId` | number | User identifier. |

## Native endpoint

Through the native actiTIME API, this operation is `GET /leavetime` (base URL `{{credentials.instanceUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-leave-time.md) for the provider-specific parameters and requirements.

