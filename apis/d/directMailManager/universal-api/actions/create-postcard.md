# Direct Mail Manager: Create Postcard



```
POST https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/create-postcard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Direct Mail Manager `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/create-postcard" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/directMailManager/latest/actions/create-postcard', {
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
      "cancelled_at": "2026-05-07T12:00:00.000Z",
      "carrier": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "mail_type": "string",
      "name": "Ava Chen",
      "object": "string",
      "size": "string",
      "status": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cancelled_at` | date |  |
| `carrier` | string |  |
| `created_at` | date |  |
| `description` | string |  |
| `id` | string |  |
| `mail_type` | string |  |
| `name` | string |  |
| `object` | string |  |
| `size` | string |  |
| `status` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Direct Mail Manager API, this operation is `POST /postcards` (base URL `https://api.directmailmanager.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-postcard.md) for the provider-specific parameters and requirements.

