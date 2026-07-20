# Abstract VAT Validator: Get VAT Categories

Retrieves VAT rate categories for a country from Abstract VAT Validator.

```
GET https://connect.mindcloud.co/v1/universal/abstractVATValidator/latest/actions/get-vat-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Abstract VAT Validator `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/abstractVATValidator/latest/actions/get-vat-categories?connectionId=$CONNECTION_ID&country_code=DE" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "country_code": "DE"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/abstractVATValidator/latest/actions/get-vat-categories?${params}`, {
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
| `country_code` | string | yes | Two-letter ISO 3166-1 alpha-2 country code to retrieve VAT categories for. Example: `DE`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "country_code": "string",
      "description": "string",
      "rate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | VAT category name. |
| `country_code` | string | Two-letter country code for the VAT category. |
| `description` | string | Description of the VAT category. |
| `rate` | string | VAT rate for the category. |

## Native endpoint

Through the native Abstract VAT Validator API, this operation is `GET /categories` (base URL `https://vat.abstractapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-vat-categories.md) for the provider-specific parameters and requirements.

