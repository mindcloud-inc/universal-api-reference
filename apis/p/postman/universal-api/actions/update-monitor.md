# Postman: Update Monitor

Updates an existing monitor in Postman.

```
PUT https://connect.mindcloud.co/v1/universal/postman/latest/actions/update-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/postman/latest/actions/update-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "monitorId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postman/latest/actions/update-monitor', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "monitorId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `monitorId` | string | yes | The monitor's ID. |
| `monitor.name` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "monitor": {
        "active": true,
        "id": "string",
        "name": "Ava Chen",
        "uid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `monitor.active` | boolean |  |
| `monitor.id` | string |  |
| `monitor.name` | string |  |
| `monitor.uid` | string |  |

## Native endpoint

Through the native Postman API, this operation is `PUT /monitors/:monitorId` (base URL `https://api.getpostman.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-monitor.md) for the provider-specific parameters and requirements.

