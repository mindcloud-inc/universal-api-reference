# Direct Mail Manager: Create Letter



```
POST https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/create-letter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Direct Mail Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/create-letter" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/create-letter', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "cancellation_time": 1,
      "cancelled_at": "2026-05-07T12:00:00.000Z",
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": "string",
      "description": "string",
      "id": "string",
      "mail_type": "string",
      "name": "Ava Chen",
      "object": "string",
      "send_date": "2026-05-07T12:00:00.000Z",
      "size": "string",
      "status": "string",
      "targets": 1,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancellation_time` | number |  |
| `cancelled_at` | date |  |
| `created_at` | date |  |
| `created_by` | string |  |
| `description` | string |  |
| `id` | string |  |
| `mail_type` | string |  |
| `name` | string |  |
| `object` | string |  |
| `send_date` | date |  |
| `size` | string |  |
| `status` | string |  |
| `targets` | number |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Direct Mail Manager API, this operation is `POST /letters` (base URL `https://api.directmailmanager.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-letter.md) for the provider-specific parameters and requirements.

