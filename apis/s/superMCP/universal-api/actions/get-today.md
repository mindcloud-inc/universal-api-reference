# SuperMCP: Get Today



```
GET https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/get-today
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperMCP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/get-today?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/get-today?${params}`, {
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
      "current_date": "2026-05-07T12:00:00.000Z",
      "current_day": 1,
      "current_month": 1,
      "current_utc": "string",
      "current_year": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_date` | date | Current UTC date. |
| `current_day` | number | Current UTC day. |
| `current_month` | number | Current UTC month. |
| `current_utc` | string | Current UTC timestamp. |
| `current_year` | number | Current UTC year. |

## Native endpoint

Through the native SuperMCP API, this operation is `POST /mcp/get_today` (base URL `https://mcp.supermetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-today.md) for the provider-specific parameters and requirements.

