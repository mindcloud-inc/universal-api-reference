# OPN: Delete Webhook Secret

Deletes an existing webhook Secret from OPN.

```
DELETE https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-webhook-secret
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-webhook-secret?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/delete-webhook-secret?${params}`, {
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
      "expires_at": "string",
      "expiring": true,
      "id": "string",
      "key": "string",
      "livemode": true,
      "object": "string",
      "revoked_at": "string",
      "usable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `expires_at` | string |  |
| `expiring` | boolean |  |
| `id` | string |  |
| `key` | string |  |
| `livemode` | boolean |  |
| `object` | string |  |
| `revoked_at` | string |  |
| `usable` | boolean |  |

## Native endpoint

Through the native OPN API, this operation is `DELETE /webhooks/secrets/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-webhook-secret.md) for the provider-specific parameters and requirements.

