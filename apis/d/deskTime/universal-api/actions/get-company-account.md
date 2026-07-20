# DeskTime: Get Company Account

Retrieves your company account details from DeskTime.

```
GET https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/get-company-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeskTime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/get-company-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/get-company-account?${params}`, {
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
      "__request_time": "string",
      "name": "Ava Chen",
      "timezone_identifier": "string",
      "work_duration": "string",
      "work_ends": "string",
      "work_start_tracking": "string",
      "work_starts": "string",
      "work_stop_tracking": "string",
      "working_days": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__request_time` | string |  |
| `name` | string |  |
| `timezone_identifier` | string |  |
| `work_duration` | string |  |
| `work_ends` | string |  |
| `work_start_tracking` | string |  |
| `work_starts` | string |  |
| `work_stop_tracking` | string |  |
| `working_days` | number |  |

## Native endpoint

Through the native DeskTime API, this operation is `GET /company` (base URL `https://desktime.com/api/v2/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-account.md) for the provider-specific parameters and requirements.

