# Scoro: List VAT Codes

Retrieves VAT codes from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-vat-codes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-vat-codes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-vat-codes?${params}`, {
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
      "is_active": 1,
      "is_not_applicable": 1,
      "is_purchases": 1,
      "is_sales": 1,
      "percent": 1,
      "vat_code": "string",
      "vat_code_id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `is_active` | number |  |
| `is_not_applicable` | number |  |
| `is_purchases` | number |  |
| `is_sales` | number |  |
| `percent` | number |  |
| `vat_code` | string |  |
| `vat_code_id` | number |  |

## Native endpoint

Through the native Scoro API, this operation is `POST vatCodes/list` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vat-codes.md) for the provider-specific parameters and requirements.

