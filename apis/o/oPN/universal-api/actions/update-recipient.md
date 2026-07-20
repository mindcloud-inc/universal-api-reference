# OPN: Update Recipient

Updates an existing recipient in OPN.

```
PUT https://connect.mindcloud.co/v1/universal/oPN/latest/actions/update-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/update-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/update-recipient', {
  method: 'PUT',
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
      "activated_at": "string",
      "active": true,
      "created_at": "string",
      "deleted": true,
      "description": "string",
      "email": "ava@example.com",
      "failure_code": "string",
      "id": "string",
      "livemode": true,
      "location": "string",
      "name": "Ava Chen",
      "object": "string",
      "type": "string",
      "verified": true,
      "verified_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activated_at` | string |  |
| `active` | boolean |  |
| `created_at` | string |  |
| `deleted` | boolean |  |
| `description` | string |  |
| `email` | string |  |
| `failure_code` | string |  |
| `id` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `name` | string |  |
| `object` | string |  |
| `type` | string |  |
| `verified` | boolean |  |
| `verified_at` | string |  |

## Native endpoint

Through the native OPN API, this operation is `PATCH /recipients/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-recipient.md) for the provider-specific parameters and requirements.

