# B2B Wave: List Suppliers

Retrieves suppliers from B2B Wave.

```
GET https://connect.mindcloud.co/v1/universal/b2BWave/latest/actions/list-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a B2B Wave `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/b2BWave/latest/actions/list-suppliers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/b2BWave/latest/actions/list-suppliers?${params}`, {
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
      "company_name": "Ava Chen",
      "email": "ava@example.com",
      "id": 1,
      "is_active": true,
      "name": "Ava Chen",
      "order_min_amount": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company_name` | string |  |
| `email` | string |  |
| `id` | number |  |
| `is_active` | boolean |  |
| `name` | string |  |
| `order_min_amount` | string |  |

## Native endpoint

Through the native B2B Wave API, this operation is `GET /suppliers` (base URL `{{credentials.storeUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-suppliers.md) for the provider-specific parameters and requirements.

