# turboSMTP: Update Alert

Updates an existing alert in turboSMTP.

```
PUT https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/update-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a turboSMTP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/update-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "Id": "9228",
  "email": "turbosmtp-alert-attempt2@example.com",
  "percentage": "85"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/update-alert', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "Id": "9228",
    "email": "turbosmtp-alert-attempt2@example.com",
    "percentage": "85"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Id` | number | yes | Alert identifier. Example: `9228`. |
| `email` | string | yes | Email address that receives the alert notification. Example: `turbosmtp-alert-attempt2@example.com`. |
| `percentage` | number | yes | Usage percentage threshold for the alert. Example: `85`. |

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
| `email` | string |  |
| `id` | number |  |
| `percentage` | number |  |

## Native endpoint

Through the native turboSMTP API, this operation is `PATCH /tools/alerts/{Id}` (base URL `https://pro.api.serversmtp.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-alert.md) for the provider-specific parameters and requirements.

