# Selock: Change Lock Status



```
PUT https://connect.mindcloud.co/v1/universal/selock/latest/actions/change-lock-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Selock `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/selock/latest/actions/change-lock-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "status": "string",
  "lock_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/selock/latest/actions/change-lock-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "status": "string",
    "lock_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | yes | Target lock status, for example open or close. |
| `lock_id` | string | yes | Sciener lock identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "res": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `res` | boolean | True when the lock status change succeeded. |

## Native endpoint

Through the native Selock API, this operation is `POST /zaiper/change_lock_status/` (base URL `https://selock.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/change-lock-status.md) for the provider-specific parameters and requirements.

