# DeskTime: List Company Employees

Retrieves company employees from DeskTime for a day or month.

```
GET https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/list-company-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DeskTime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/list-company-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deskTime/latest/actions/list-company-employees?${params}`, {
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
| `date` | string | no | Date in YYYY-MM-DD format. Example: `2026-03-24`. |
| `period` | string | no | Tracking period. One of: `0`, `1`. Default: `day`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "__request_time": "string",
      "employees": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `__request_time` | string |  |
| `employees` | object |  |

## Native endpoint

Through the native DeskTime API, this operation is `GET /employees` (base URL `https://desktime.com/api/v2/json`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-company-employees.md) for the provider-specific parameters and requirements.

