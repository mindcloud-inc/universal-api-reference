# OPN: Delete Linked Account

Deletes an existing linked Account from OPN.

```
DELETE https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-linked-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-linked-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-linked-account?${params}`, {
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
      "created_at": "string",
      "customer_id": "string",
      "expires_at": "string",
      "id": "string",
      "last_digits": "string",
      "livemode": true,
      "location": "string",
      "object": "string",
      "registered_at": "string",
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `customer_id` | string |  |
| `expires_at` | string |  |
| `id` | string |  |
| `last_digits` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `object` | string |  |
| `registered_at` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native OPN API, this operation is `DELETE /linked_accounts/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-linked-account.md) for the provider-specific parameters and requirements.

