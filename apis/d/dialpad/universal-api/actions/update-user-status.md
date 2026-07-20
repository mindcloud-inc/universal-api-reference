# Dialpad: Update User Status

Updates a user's status in Dialpad.

```
PUT https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/update-user-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dialpad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/update-user-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dialpad/latest/actions/update-user-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The user's id. |
| `status_message` | string | no | The status message for the user. |
| `expiration` | number | no | The expiration of this status. None for no expiration. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expiration": 1,
      "id": "string",
      "statusMessage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expiration` | number |  |
| `id` | string |  |
| `statusMessage` | string |  |

## Native endpoint

Through the native Dialpad API, this operation is `PATCH /users/:id/status` (base URL `https://dialpad.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-user-status.md) for the provider-specific parameters and requirements.

