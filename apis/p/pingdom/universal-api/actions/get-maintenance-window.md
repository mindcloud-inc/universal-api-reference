# Pingdom: Get Maintenance Window



```
GET https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/get-maintenance-window
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingdom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/get-maintenance-window?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/get-maintenance-window?${params}`, {
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
| `id` | number | yes | Identifier of the maintenance window. |

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

Through the native Pingdom API, this operation is `GET /maintenance/:id` (base URL `https://api.pingdom.com/api/3.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-maintenance-window.md) for the provider-specific parameters and requirements.

