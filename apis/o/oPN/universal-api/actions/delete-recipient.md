# OPN: Delete Recipient

Deletes an existing recipient from OPN.

```
DELETE https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-recipient
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-recipient?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-recipient?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
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
      "deleted": true,
      "email": "ava@example.com",
      "id": "string",
      "livemode": true,
      "location": "string",
      "name": "Ava Chen",
      "object": "string",
      "type": "string",
      "verified": true
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
| `deleted` | boolean |  |
| `email` | string |  |
| `id` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `name` | string |  |
| `object` | string |  |
| `type` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native OPN API, this operation is `DELETE /recipients/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-recipient.md) for the provider-specific parameters and requirements.

