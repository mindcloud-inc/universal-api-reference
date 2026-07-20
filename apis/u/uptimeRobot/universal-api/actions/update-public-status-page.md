# UptimeRobot: Update Public Status Page

Updates an existing public status page in UptimeRobot.

```
PUT https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/update-public-status-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UptimeRobot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/update-public-status-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "type": 1,
  "friendly_name": "Ava Chen",
  "monitors": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uptimeRobot/latest/actions/update-public-status-page', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "type": 1,
    "friendly_name": "Ava Chen",
    "monitors": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the status page to update. |
| `type` | number | yes | Status page type. Legacy docs examples use 1. |
| `friendly_name` | string | yes | Status page display name. |
| `monitors` | string | yes | Dash-separated monitor IDs to display, or 0 for all monitors. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "psp": {},
      "stat": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `psp` | object |  |
| `stat` | string |  |

## Native endpoint

Through the native UptimeRobot API, this operation is `POST /editPSP` (base URL `https://api.uptimerobot.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-public-status-page.md) for the provider-specific parameters and requirements.

