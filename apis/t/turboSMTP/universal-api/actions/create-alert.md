# turboSMTP: Create Alert

Creates a new alert in turboSMTP.

```
POST https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/create-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a turboSMTP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/create-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "turbosmtp-alert-attempt2@example.com",
  "percentage": "80"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/create-alert', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "turbosmtp-alert-attempt2@example.com",
    "percentage": "80"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Email address that receives the alert notification. Example: `turbosmtp-alert-attempt2@example.com`. |
| `percentage` | number | yes | Usage percentage threshold for the alert. Example: `80`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": 1,
      "percentage": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Alert notification email address. |
| `id` | number | Alert ID. |
| `percentage` | number | Usage percentage threshold. |

## Native endpoint

Through the native turboSMTP API, this operation is `POST /tools/alerts` (base URL `https://pro.api.serversmtp.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-alert.md) for the provider-specific parameters and requirements.

