# Seven Time: List Work Schedules

Retrieves work schedules from Seven Time.

```
GET https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-work-schedules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Seven Time `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-work-schedules?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sevenTime/latest/actions/list-work-schedules?${params}`, {
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
      "description": "string",
      "Id": "string",
      "isActive": true,
      "name": "Ava Chen",
      "workScheduleWeeks": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `Id` | string |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `workScheduleWeeks` | array<object> |  |

## Native endpoint

Through the native Seven Time API, this operation is `GET /workSchedules` (base URL `https://app.seventime.se/api/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-work-schedules.md) for the provider-specific parameters and requirements.

