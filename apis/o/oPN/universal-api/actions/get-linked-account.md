# OPN: Get Linked Account

Retrieves details for a linked Account from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-linked-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-linked-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-linked-account?${params}`, {
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
      "failure_code": "string",
      "failure_message": "string",
      "id": "string",
      "last_digits": "string",
      "livemode": true,
      "location": "string",
      "metadata": {},
      "object": "string",
      "registered_at": "string",
      "registration_uri": "string",
      "return_uri": "string",
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
| `failure_code` | string |  |
| `failure_message` | string |  |
| `id` | string |  |
| `last_digits` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `metadata` | object |  |
| `object` | string |  |
| `registered_at` | string |  |
| `registration_uri` | string |  |
| `return_uri` | string |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native OPN API, this operation is `GET /linked_accounts/:id` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-linked-account.md) for the provider-specific parameters and requirements.

