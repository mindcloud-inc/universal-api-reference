# Uku: List Invoice Sellers

Retrieves invoice sellers from Uku.

```
GET https://connect.mindcloud.co/v1/universal/uku/latest/actions/list-invoice-sellers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uku `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uku/latest/actions/list-invoice-sellers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uku/latest/actions/list-invoice-sellers?${params}`, {
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
      "address": "string",
      "bank_1": "string",
      "bank_2": "string",
      "company_id": 1,
      "company_number": "string",
      "created_at": "string",
      "iban_1": "string",
      "iban_2": "string",
      "id": 1,
      "logo_url": "https://example.com",
      "name": "Ava Chen",
      "status": "string",
      "updated_at": "string",
      "vat_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `bank_1` | string |  |
| `bank_2` | string |  |
| `company_id` | number |  |
| `company_number` | string |  |
| `created_at` | string |  |
| `iban_1` | string |  |
| `iban_2` | string |  |
| `id` | number |  |
| `logo_url` | string |  |
| `name` | string |  |
| `status` | string |  |
| `updated_at` | string |  |
| `vat_number` | string |  |

## Native endpoint

Through the native Uku API, this operation is `GET /invoice_sellers` (base URL `https://app.getuku.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-invoice-sellers.md) for the provider-specific parameters and requirements.

