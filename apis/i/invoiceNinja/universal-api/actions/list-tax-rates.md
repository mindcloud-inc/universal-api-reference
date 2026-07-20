# Invoice Ninja: List Tax Rates



```
GET https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-tax-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice Ninja `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-tax-rates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-tax-rates?${params}`, {
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
      "archived_at": 1,
      "created_at": 1,
      "id": "string",
      "is_deleted": true,
      "name": "Ava Chen",
      "rate": 1,
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived_at` | number |  |
| `created_at` | number |  |
| `id` | string |  |
| `is_deleted` | boolean |  |
| `name` | string |  |
| `rate` | number |  |
| `updated_at` | number |  |

## Native endpoint

Through the native Invoice Ninja API, this operation is `GET /tax_rates` (base URL `https://invoicing.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tax-rates.md) for the provider-specific parameters and requirements.

