# Cursion: Create Alert



```
POST https://connect.mindcloud.co/v1/universal/cursion/latest/actions/create-alert
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cursion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cursion/latest/actions/create-alert" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "actions": {},
  "expressions": {},
  "name": "Ava Chen",
  "siteId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cursion/latest/actions/create-alert', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "actions": {},
    "expressions": {},
    "name": "Ava Chen",
    "siteId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actions` | list<object> | yes | The list of alert action objects. |
| `expressions` | list<object> | yes | The list of alert expression objects. |
| `name` | string | yes | The alert display name. |
| `scheduleId` | string | no | The optional schedule to attach this alert to. |
| `siteId` | string | yes | The site identifier for the alert. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account": "string",
      "actions": [
        {}
      ],
      "expressions": [
        {}
      ],
      "id": "string",
      "name": "Ava Chen",
      "schedule": "string",
      "time_created": "string",
      "user": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account` | string |  |
| `actions` | array<object> |  |
| `expressions` | array<object> |  |
| `id` | string |  |
| `name` | string |  |
| `schedule` | string |  |
| `time_created` | string |  |
| `user` | string |  |

## Native endpoint

Through the native Cursion API, this operation is `POST /alert` (base URL `https://api.cursion.dev/v1/ops`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-alert.md) for the provider-specific parameters and requirements.

