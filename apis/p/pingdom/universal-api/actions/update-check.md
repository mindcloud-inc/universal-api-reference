# Pingdom: Update Check



```
PUT https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/update-check
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pingdom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/update-check" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checkId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pingdom/latest/actions/update-check', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checkId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checkId` | number | yes | Identifier of the check to update. |
| `name` | string | no | Updated check name. |
| `host` | string | no | Updated target host. |
| `paused` | boolean | no | Pause or unpause the check. |
| `resolution` | number | no | Updated check interval in minutes. |
| `userIds` | string | no | Comma-separated list of user identifiers to alert. |
| `sendNotificationWhenDown` | number | no | Send a notification when the check has been down this many times. |
| `notifyAgainEvery` | number | no | Send another notification every n results. Use 0 to disable repeat notifications. |
| `notifyWhenBackUp` | boolean | no | Notify again when the check is back up. |
| `tags[]` | array<string> | no | Replace the check tags with this list. |
| `addTags[]` | array<string> | no | Tags to add without replacing the current tag list. |
| `probeFilters[]` | array<string> | no | Updated probe selection filters such as region filters. |
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider confirmation message. |

## Native endpoint

Through the native Pingdom API, this operation is `PUT /checks/:checkid` (base URL `https://api.pingdom.com/api/3.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-check.md) for the provider-specific parameters and requirements.

