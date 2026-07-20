# Testomato: Update notifications

Updates project notification settings in Testomato.

```
PUT https://connect.mindcloud.co/v1/universal/testomato/latest/actions/update-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Testomato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/testomato/latest/actions/update-notifications" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testomato/latest/actions/update-notifications', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `severity` | number | no |  |
| `email` | boolean | no |  |
| `pagerduty` | boolean | no |  |
| `pushover` | boolean | no |  |
| `pushbullet` | boolean | no |  |
| `slack` | boolean | no |  |
| `webhook` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": true,
      "pagerduty": true,
      "pushbullet": true,
      "pushover": true,
      "severity": 1,
      "slack": true,
      "webhook": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | boolean |  |
| `pagerduty` | boolean |  |
| `pushbullet` | boolean |  |
| `pushover` | boolean |  |
| `severity` | number |  |
| `slack` | boolean |  |
| `webhook` | boolean |  |

## Native endpoint

Through the native Testomato API, this operation is `POST /project/:id/notifications` (base URL `https://testomato.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-notifications.md) for the provider-specific parameters and requirements.

