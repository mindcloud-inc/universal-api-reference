# ChargeBee: List Virtual Bank Accounts

Retrieves virtual bank accounts from ChargeBee.

```
GET https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-virtual-bank-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChargeBee `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-virtual-bank-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeBee/latest/actions/list-virtual-bank-accounts?${params}`, {
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
      "account_number": "string",
      "bank_name": "Ava Chen",
      "created_at": 1,
      "customer_id": "string",
      "id": "string",
      "object": "string",
      "reference_id": "string",
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_number` | string |  |
| `bank_name` | string |  |
| `created_at` | number |  |
| `customer_id` | string |  |
| `id` | string |  |
| `object` | string |  |
| `reference_id` | string |  |
| `updated_at` | number |  |

## Native endpoint

Through the native ChargeBee API, this operation is `GET virtual_bank_accounts` (base URL `https://{{credentials.baseUrl}}.chargebee.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-virtual-bank-accounts.md) for the provider-specific parameters and requirements.

