# Pingdom: Update Maintenance Window



```
PUT https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/update-maintenance-window
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingdom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/update-maintenance-window" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/update-maintenance-window', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | Identifier of the maintenance window. |
| `description` | string | no | Maintenance window description. |
| `from` | number | no | Initial maintenance start as UNIX time. |
| `to` | number | no | Initial maintenance end as UNIX time. |
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Pingdom API, this operation is `PUT /maintenance/:id` (base URL `https://api.pingdom.com/api/3.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-maintenance-window.md) for the provider-specific parameters and requirements.

