# Geral: List Account Logs

Retrieves account logs from Geral.

```
GET https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-account-logs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-account-logs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/list-account-logs?${params}`, {
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
      "city_name": "Ava Chen",
      "continent_code": "string",
      "country_code": "string",
      "datetime": "2026-05-07T12:00:00.000Z",
      "device_type": "string",
      "id": 1,
      "ip": "string",
      "os_name": "Ava Chen",
      "type": "string",
      "user_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city_name` | string | City name. |
| `continent_code` | string | Continent code. |
| `country_code` | string | Country code. |
| `datetime` | date | Event timestamp. |
| `device_type` | string | Device type. |
| `id` | number | Account log ID. |
| `ip` | string | IP address. |
| `os_name` | string | Operating system name. |
| `type` | string | Account log event type. |
| `user_id` | number | User ID. |

## Native endpoint

Through the native Geral API, this operation is `GET /logs/` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-account-logs.md) for the provider-specific parameters and requirements.

