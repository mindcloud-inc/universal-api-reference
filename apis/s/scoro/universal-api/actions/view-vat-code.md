# Scoro: View VAT Code

Retrieves VAT code details from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-vat-code
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-vat-code?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-vat-code?${params}`, {
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
| `id` | string | no | Scoro VAT code ID. |

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
      "vat_code_id": 1,
      "vat_name": "Ava Chen"
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
| `vat_name` | string |  |

## Native endpoint

Through the native Scoro API, this operation is `POST vatCodes/view/:id` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-vat-code.md) for the provider-specific parameters and requirements.

