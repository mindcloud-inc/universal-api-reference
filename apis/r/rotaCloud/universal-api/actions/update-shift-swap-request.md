# RotaCloud: Update Shift Swap Request



```
PUT https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-shift-swap-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-shift-swap-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "admin_approved": true,
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/update-shift-swap-request', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "admin_approved": true,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `admin_approved` | boolean | yes | Whether the admin approved the swap request. |
| `id` | number | yes | Shift swap request ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin": 1,
      "admin_approved": true,
      "admin_replied_at": 1,
      "deleted": true,
      "id": 1,
      "new_user": 1,
      "old_user": 1,
      "requested_at": 1,
      "shift": 1,
      "status": "string",
      "swapped_shift": 1,
      "user_approved": true,
      "user_replied_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | number |  |
| `admin_approved` | boolean |  |
| `admin_replied_at` | number |  |
| `deleted` | boolean |  |
| `id` | number |  |
| `new_user` | number |  |
| `old_user` | number |  |
| `requested_at` | number |  |
| `shift` | number |  |
| `status` | string |  |
| `swapped_shift` | number |  |
| `user_approved` | boolean |  |
| `user_replied_at` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `POST /v1/swap_requests/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-shift-swap-request.md) for the provider-specific parameters and requirements.

