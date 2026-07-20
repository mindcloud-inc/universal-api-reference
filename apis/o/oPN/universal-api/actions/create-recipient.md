# OPN: Create Recipient

Creates a new recipient in OPN.

```
POST https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/create-recipient', {
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

Through the native OPN API, this operation is `POST /recipients` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recipient.md) for the provider-specific parameters and requirements.

