# DivvyHQ: Patch Simple Calendar



```
PUT https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/patch-simple-calendar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DivvyHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/patch-simple-calendar" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/patch-simple-calendar', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "account": 1,
      "defaultDeadlineTime": "string",
      "editable": true,
      "id": 1,
      "isEnterprise": true,
      "isHidden": true,
      "kind": "string",
      "name": "Ava Chen",
      "parentCalendar": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | number | The Divvy account id. |
| `defaultDeadlineTime` | string | The default deadline time. |
| `editable` | boolean | Whether the calendar is editable. |
| `id` | number | The calendar id. |
| `isEnterprise` | boolean | Whether the calendar is enterprise scoped. |
| `isHidden` | boolean | Whether the calendar is hidden. |
| `kind` | string | The calendar kind. |
| `name` | string | The calendar name. |
| `parentCalendar` | number | The parent calendar id when present. |

## Native endpoint

Through the native DivvyHQ API, this operation is `PATCH /simplecalendars/:id/` (base URL `https://app.divvyhq.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/patch-simple-calendar.md) for the provider-specific parameters and requirements.

