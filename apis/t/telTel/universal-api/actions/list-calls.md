# TelTel: List Calls

Retrieves calls from your TelTel account.

```
GET https://connect.mindcloud.co/v1/universal/telTel/latest/actions/list-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TelTel `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/telTel/latest/actions/list-calls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/telTel/latest/actions/list-calls?${params}`, {
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
      "callId": "string",
      "cost": 1,
      "direction": "string",
      "durationSec": 1,
      "starttime": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "stoptime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `callId` | string |  |
| `cost` | number |  |
| `direction` | string |  |
| `durationSec` | number |  |
| `starttime` | date |  |
| `status` | string |  |
| `stoptime` | date |  |

## Native endpoint

Through the native TelTel API, this operation is `GET /calls` (base URL `https://api.teltel.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-calls.md) for the provider-specific parameters and requirements.

