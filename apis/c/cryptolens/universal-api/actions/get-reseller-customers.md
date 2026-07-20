# Cryptolens: Get Reseller Customers

Retrieves customers for a reseller from Cryptolens.

```
GET https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-reseller-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cryptolens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-reseller-customers?connectionId=$CONNECTION_ID&resellerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resellerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/get-reseller-customers?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resellerId` | number | yes | The reseller id. |

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
| `companyName` | string | Get Reseller Customers response field `companyName` from Cryptolens docs example. |
| `created` | string | Get Reseller Customers response field `created` from Cryptolens docs example. |
| `email` | string | Get Reseller Customers response field `email` from Cryptolens docs example. |
| `id` | number | Get Reseller Customers response field `id` from Cryptolens docs example. |
| `name` | string | Get Reseller Customers response field `name` from Cryptolens docs example. |

## Native endpoint

Through the native Cryptolens API, this operation is `GET /api/reseller/GetResellerCustomers` (base URL `https://api.cryptolens.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-reseller-customers.md) for the provider-specific parameters and requirements.

