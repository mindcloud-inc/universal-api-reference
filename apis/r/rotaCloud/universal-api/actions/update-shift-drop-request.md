# RotaCloud: Update Shift Drop Request



```
PUT https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-shift-drop-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-shift-drop-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "decision": "string",
  "id": 1,
  "user_message": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-shift-drop-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "decision": "string",
    "id": 1,
    "user_message": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `decision` | string | yes | Decision path segment, such as approve or deny. |
| `id` | number | yes | Shift drop request ID. |
| `user_message` | string | yes | Reply message for the shift drop request. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin": 1,
      "admin_message": "string",
      "deleted": true,
      "id": 1,
      "replied_at": 1,
      "requested_at": 1,
      "shift": 1,
      "status": "string",
      "user": 1,
      "user_message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | number |  |
| `admin_message` | string |  |
| `deleted` | boolean |  |
| `id` | number |  |
| `replied_at` | number |  |
| `requested_at` | number |  |
| `shift` | number |  |
| `status` | string |  |
| `user` | number |  |
| `user_message` | string |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/unavailability_requests/:id/:decision` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shift-drop-request.md) for the provider-specific parameters and requirements.

