# Pingdom: Create Maintenance Window



```
POST https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/create-maintenance-window
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingdom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/create-maintenance-window" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "description": "string",
  "from": 1,
  "to": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/create-maintenance-window', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "description": "string",
    "from": 1,
    "to": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | yes | Maintenance window description. |
| `from` | number | yes | Initial maintenance start as UNIX time. |
| `to` | number | yes | Initial maintenance end as UNIX time. |
| `recurrenceType` | string | no | Recurrence type. |
| `repeatEvery` | number | no | Repeat every n-th interval. |
| `effectiveTo` | number | no | Recurrence end as UNIX time. |
| `uptimeIds[]` | array<number> | no | Uptime checks assigned to the maintenance window. |
| `tmsIds[]` | array<number> | no | Transaction checks assigned to the maintenance window. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native Pingdom API, this operation is `POST /maintenance` (base URL `https://api.pingdom.com/api/3.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-maintenance-window.md) for the provider-specific parameters and requirements.

