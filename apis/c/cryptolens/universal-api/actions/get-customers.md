# Cryptolens: Get Customers

Retrieves customers from Cryptolens.

```
GET https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptolens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-customers?${params}`, {
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
      "companyName": "Ava Chen",
      "created": "string",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string | Get Customers response field `companyName` from Cryptolens docs example. |
| `created` | string | Get Customers response field `created` from Cryptolens docs example. |
| `email` | string | Get Customers response field `email` from Cryptolens docs example. |
| `id` | number | Get Customers response field `id` from Cryptolens docs example. |
| `name` | string | Get Customers response field `name` from Cryptolens docs example. |

## Native endpoint

Through the native Cryptolens API, this operation is `GET /api/customer/GetCustomers` (base URL `https://api.cryptolens.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customers.md) for the provider-specific parameters and requirements.

