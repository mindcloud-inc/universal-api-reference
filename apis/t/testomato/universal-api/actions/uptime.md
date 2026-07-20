# Testomato: Uptime

Retrieves project uptime data from Testomato.

```
GET https://connect.mindcloud.co/v1/universal/testomato/latest/actions/uptime
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testomato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testomato/latest/actions/uptime?connectionId=$CONNECTION_ID&id=string&start=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "start": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testomato/latest/actions/uptime?${params}`, {
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
| `id` | string | yes |  |
| `start` | date | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "daysCount": 1,
      "from": "string",
      "isUptimeEnabled": 1,
      "to": "string",
      "uptime": {},
      "uptimeByDays": [
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
| `daysCount` | number |  |
| `from` | string |  |
| `isUptimeEnabled` | number |  |
| `to` | string |  |
| `uptime` | object |  |
| `uptimeByDays` | array<object> |  |

## Native endpoint

Through the native Testomato API, this operation is `GET /project/:id/uptime` (base URL `https://testomato.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/uptime.md) for the provider-specific parameters and requirements.

