# InvoiceBerry: List Clients



```
GET https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InvoiceBerry `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceBerry/latest/actions/list-clients?${params}`, {
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
| `limit` | number | no | Default: `20`. |
| `offset` | number | no | Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "client_name": "Ava Chen",
      "country": "string",
      "country_iso": "string",
      "currency": "string",
      "fax": "string",
      "id": "string",
      "language": "string",
      "notes": "string",
      "phone": "string",
      "state": "string",
      "street1": "string",
      "street2": "string",
      "tax_name": "Ava Chen",
      "tax_number": "string",
      "zip_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string | City. |
| `client_name` | string | Client display name. |
| `country` | string | Country name. |
| `country_iso` | string | ISO alpha-2 country code. |
| `currency` | string | Client currency. |
| `fax` | string | Fax number. |
| `id` | string | InvoiceBerry client identifier. |
| `language` | string | Client language. |
| `notes` | string | Client notes. |
| `phone` | string | Primary phone number. |
| `state` | string | State or region. |
| `street1` | string | Address line 1. |
| `street2` | string | Address line 2. |
| `tax_name` | string | Tax label. |
| `tax_number` | string | Tax registration number. |
| `zip_code` | string | Postal code. |

## Native endpoint

Through the native InvoiceBerry API, this operation is `POST /api` (base URL `https://www.invoiceberry.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

