# Pingdom: Create Check



```
POST https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/create-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingdom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/create-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "host": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/create-check', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "host": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Check name. |
| `host` | string | yes | Target host for the check. |
| `type` | string | yes | Type of check to create. |
| `paused` | boolean | no | Pause the check immediately after creation. |
| `resolution` | number | no | How often the check should run, in minutes. |
| `userIds` | string | no | Comma-separated list of user identifiers to alert. |
| `sendNotificationWhenDown` | number | no | Send a notification when the check has been down this many times. |
| `notifyAgainEvery` | number | no | Send another notification every n results. Use 0 to disable repeat notifications. |
| `notifyWhenBackUp` | boolean | no | Notify again when the check is back up. |
| `tags[]` | array<string> | no | Tags to assign to the check. |
| `probeFilters[]` | array<string> | no | Probe selection filters such as region filters. |
| `ipv6` | boolean | no | Use IPv6 instead of IPv4 when applicable. |
| `responseTimeThreshold` | number | no | Response-time threshold in milliseconds that triggers a down alert. |
| `integrationIds[]` | array<number> | no | Integration identifiers to associate with the check. |
| `teamIds` | string | no | Comma-separated team identifiers to alert. |
| `customMessage` | string | no | Custom message appended to email and webhook alerts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Created check identifier. |
| `name` | string | Created check name. |

## Native endpoint

Through the native Pingdom API, this operation is `POST /checks` (base URL `https://api.pingdom.com/api/3.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-check.md) for the provider-specific parameters and requirements.

