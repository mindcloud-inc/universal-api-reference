# OPN: Verify Recipient

Verifies an existing recipient in OPN.

```
PUT https://connect.mindcloud.co/v1/universal/oPN/latest/actions/verify-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/verify-recipient" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oPN/latest/actions/verify-recipient', {
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
      "active": true,
      "created_at": "string",
      "email": "ava@example.com",
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
| `active` | boolean |  |
| `created_at` | string |  |
| `email` | string |  |
| `id` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `name` | string |  |
| `object` | string |  |
| `type` | string |  |
| `verified` | boolean |  |
| `verified_at` | string |  |

## Native endpoint

Through the native OPN API, this operation is `PATCH /recipients/:id/verify` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-recipient.md) for the provider-specific parameters and requirements.

