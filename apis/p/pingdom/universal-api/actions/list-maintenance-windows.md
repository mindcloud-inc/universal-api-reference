# Pingdom: List Maintenance Windows



```
GET https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/list-maintenance-windows
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingdom `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/list-maintenance-windows?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/list-maintenance-windows?${params}`, {
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
| `orderBy` | string | no | Order by the selected maintenance field. |
| `order` | string | no | Sort direction. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "checks": {},
      "dayofweekinmonth": 1,
      "description": "string",
      "duration": 1,
      "durationunit": "string",
      "effectiveto": 1,
      "from": 1,
      "id": 1,
      "recurrencetype": "string",
      "repeatevery": 1,
      "to": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `checks` | object |  |
| `dayofweekinmonth` | number |  |
| `description` | string |  |
| `duration` | number |  |
| `durationunit` | string |  |
| `effectiveto` | number |  |
| `from` | number |  |
| `id` | number |  |
| `recurrencetype` | string |  |
| `repeatevery` | number |  |
| `to` | number |  |

## Native endpoint

Through the native Pingdom API, this operation is `GET /maintenance` (base URL `https://api.pingdom.com/api/3.1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-maintenance-windows.md) for the provider-specific parameters and requirements.

